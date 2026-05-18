# Server Installation

## 테스트 환경

- Server Type : Linux
- Server OS : Rocky linux 8.9

## 필요 패키지 설치

### 운영체제 기본 설정

```Bash
sudo dnf update -y
sudo dnf install -y epel-release
```

```Bash
sudo dnf install -y curl wget git vim tar net-tools \
  yum-utils device-mapper-persistent-data lvm2
```

### Docker / Containerd 설치

SCALE.sdm은 Kubernetes 기반이므로 컨테이너 런타임 필요

```Bash
sudo dnf config-manager --add-repo=https://download.docker.com/linux/centos/docker-ce.repo
sudo dnf install -y docker-ce docker-ce-cli containerd.io
```

:::{admonition} Podman/Buildah 패키지 충돌
:class: notice

- Rocky Linux 8.x는 기본적으로 Podman/Buildah (CRI-O)를 컨테이너 런타임으로 사용
- Docker CE를 설치하면 containerd.io, runc가 같이 들어오는데, 이미 설치된 Podman/Buildah가 같은 runc에 의존해서 충돌 발생
- 따라서 Podman/Buildah 를 제거하거나, DNF module 스트림을 비활성화해주어야 Docker CE 설치가 가능합니다.
- Podman/Buildah 제거
  
```Bash
sudo dnf remove -y podman buildah
```
  
- runc 모듈 스트림 리젯

```Bash
sudo dnf module reset -y container-tools
```

- 다시 Docker CE 설치
  
```Bash
sudo dnf install -y docker-ce docker-ce-cli containerd.io --allowerasing
```

:::

### containerd 설정

#### containerd 설치

```Bash
sudo dnf install -y containerd
```

#### 설정 파일 생성

```Bash
sudo mkdir -p /etc/containerd
sudo containerd config default | sudo tee /etc/containerd/config.toml
```

#### Cgroup 드라이버를 systemd로 변경

```Bash
sudo sed -i 's/SystemdCgroup = false/SystemdCgroup = true/' /etc/containerd/config.toml
```

#### 서비스 활성화

```Bash
sudo systemctl enable --now containerd
```

### runc 및 CNI 플러그인 설정

#### 설치

```Bash
sudo dnf install -y runc
```

#### CNI 플러그인 다운로드 (예: 1.3.0)

```Bash
wget https://github.com/containernetworking/plugins/releases/download/v1.3.0/cni-plugins-linux-amd64-v1.3.0.tgz
sudo mkdir -p /opt/cni/bin
sudo tar Cxzvf /opt/cni/bin cni-plugins-linux-amd64-v1.3.0.tgz
```

### Kubernetes 패키지 설치

#### Kubernetes YUM repo 등록

```Bash
cat <<EOF | sudo tee /etc/yum.repos.d/kubernetes.repo
[kubernetes]
name=Kubernetes
baseurl=https://pkgs.k8s.io/core:/stable:/v1.29/rpm/
enabled=1
gpgcheck=1
gpgkey=https://pkgs.k8s.io/core:/stable:/v1.29/rpm/repodata/repomd.xml.key
EOF
```

#### Kubernetes 설치

```Bash
sudo dnf install -y kubelet kubeadm kubectl
sudo systemctl enable --now kubelet
```

#### Swap 비활성화

```Bash
sudo swapoff -a
sudo sed -i '/ swap / s/^/#/' /etc/fstab
```

### 마스터 노드 초기화

#### 선행으로 확인해야할 사항

- kubelet이 실행중인지 확인
  
```Bash
sudo systemctl daemon-reload
sudo systemctl restart kubelet
sudo systemctl enable kubelet
```

```Bash
sudo kubeadm init \
  --apiserver-advertise-address=192.168.100.100 \
  --pod-network-cidr=10.244.0.0/16
```

:::{admonition} 주의사항
Master와 Worker 노드의 연결을 위해 Master와 Worker 노드간에 네트워크 연결이 된 호스트(IP)를 사용해야 합니다.

```Bash
# 워커의 인터페이스와 IP 확인
ip addr show

# 라우팅 테이블 확인
ip route show

# 마스터 IP들(두 대역)에 대한 연결 테스트
ping -c3 192.168.1.129
ping -c3 192.168.100.100

# 포트 연결 테스트 (nc)
nc -vz 192.168.1.129 6443
nc -vz 192.168.100.100 6443

# 라우팅 경로 추적(있으면)
traceroute -n 192.168.1.129
```

연결이 가능한 호스트에 대해서 --apiserver-advertise-address={확인된 호스트} 옵션을 주고 초기화 합니다.

:::

:::{note}
kubeadm init에서 출력되는 join 명령어를 Worker node join에 사용합니다.
:::

### kubectl 환경 설정

```Bash
mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config
```

### Pod Network 설치

```Bash
kubectl apply -f https://raw.githubusercontent.com/flannel-io/flannel/master/Documentation/kube-flannel.yml
```

### Worker Node 설정

```Bash
# 1. Container Runtime 설치 (예: containerd)
sudo yum install -y containerd
sudo systemctl enable --now containerd

# 2. Kubernetes repo 추가
cat <<EOF | sudo tee /etc/yum.repos.d/kubernetes.repo
[kubernetes]
name=Kubernetes
baseurl=https://packages.cloud.google.com/yum/repos/kubernetes-el7-x86_64
enabled=1
gpgcheck=1
repo_gpgcheck=1
gpgkey=https://packages.cloud.google.com/yum/doc/yum-key.gpg
       https://packages.cloud.google.com/yum/doc/rpm-package-key.gpg
EOF

# 3. kubeadm, kubelet 설치
sudo yum install -y kubeadm kubelet kubectl
sudo systemctl enable --now kubelet

# 4. swap off (필수)
sudo swapoff -a
```

:::{admonition} 네트워크 연결이 되지 않는 환경에서의 설정
:class: note
외부와 네트워크 연결이 되는 노드에서 yumdownloader를 사용하여 rpm 다운로드 후 설치

```Bash
yumdownloader --resolve --arch=x86_64 kubeadm-1.29.15 kubelet-1.29.15 kubectl-1.29.15

# 의존하는 패키지 다운로드
yumdownloader --resolve --arch=x86_64 cri-tools kubernetes-cni

# containerd 패키지 다운로드
yumdownloader --resolve --arch=x86_64 containerd
```

설치는 아래와 같이 진행합니다.

```Bash
sudo yum localinstall -y *.rpm
```

설치 후 containerd 및 kubelet 실행 확인 및 실행

```Bash
sudo systemctl start containerd
sudo systemctl enable --now kubelet
sudo systemctl status kubelet
```

```Bash
# br-netfilter 모듈 로드
sudo modprobe br_netfilter

# 모듈이 부팅 시 자동 로드되도록 설정
echo "br_netfilter" | sudo tee /etc/modules-load.d/br_netfilter.conf

# sysctl 설정 추가
cat <<EOF | sudo tee /etc/sysctl.d/k8s.conf
net.bridge.bridge-nf-call-iptables = 1
net.bridge.bridge-nf-call-ip6tables = 1
net.ipv4.ip_forward = 1
EOF

# sysctl 적용
sudo sysctl --system

# 적용 확인 -> 모두 = 1 이어야 정상
sysctl net.bridge.bridge-nf-call-iptables
sysctl net.bridge.bridge-nf-call-ip6tables
sysctl net.ipv4.ip_forward

```

:::

#### Worker에서 노드 join

```Bash
sudo kubeadm join 192.168.100.100:6443 \
  --token <TOKEN> \
  --discovery-token-ca-cert-hash sha256:<HASH>
```

#### Join 결과 확인

```Bash
kubectl get nodes

# 출력 내용
NAME            STATUS   ROLES           AGE   VERSION
snode01         Ready    <none>          1m    v1.29.15
snodemaster01   Ready    control-plane   10m   v1.29.15
```
## DNS 서버 구성

### bind9 설치 및 활성화

bind는 DNS 서버를 구축 및 운영하기 위한 표준 서버 데몬 프로그램으로 유닉스 및 리눅스, 윈도우 등 거의 모든 플랫폼을 지원하는 DNS의 모든 기능을 갖춘 소프트웨어

named는 네임서버 데이터베이스 및 root zone 파일의 위치, root 파일, key 파일, 접근제어등의 보안설정을 하는 bind 메인 설정 파일이며 bind를 설치하면 /etc/named.conf 설정파일이 존재함

```Bash
sudo dnf install bind bind-utils -y
systemctl enable --now named
```

#### named 리슨 설정 확인

/etc/named.conf
```Bash
options {
  listen-on port 53 { any; };
  listen-on-v6 { none; };
  allow-query { any; };
};
```

수정 후 
```Bash
systemctl restart named
```

:::{caution}
방화벽 문제가 있을 수 있으므로 DNS 포트를 개방하거나 방화벽 시스템을 disable
```Bash
firewall-cmd --add-service=dns --permanent
firewall-cmd --reload

또는 명시적으로

firewall-cmd --add-port=53/udp --permanent
firewall-cmd --add-port=53/tcp --permanent
firewall-cmd --reload
```
:::