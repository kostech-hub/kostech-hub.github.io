# Contents

- [OASYS 라이선스 신청 및 적용 방법](#oasys-라이선스-신청-및-적용-방법)
<br />

    - [라이선스 신청](#라이선스-신청)


## OASYS 라이선스 신청 및 적용 방법

### 라이선스 신청

#### 1. Floating license on linux server

linux 장비에 아래 링크에서 라이선스 서버 설치 파일을 다운로드 받거나 혹은 linux 서버에 curl이 설치되어 있다면 curl를 사용하여 다운로드 받습니다.

https://www.oasys-software.com/dyna/downloads/server-licensing

``` bash
curl -O https://www.oasys-software.com/dyna/wp-content/uploads/2022/03/sudo-lmx-5.2_rhel7.tar.gz # 파일 다운로드
```

다운로드 받은 파일의 압축을 해제하고 설치를 진행합니다. 설치 진행 시 설치 경로를 묻는 메세지가 나오는데 내용을 참고하여 진행합니다.

``` bash
tar -zxvf sudo-lmx-5.2_rhel7.tar.gz     # 압축 해제
cd sudo-lmx-5.2_rhel7                   # 폴더 이동
./sudo_lmx_install.csh                  # 설치
```


