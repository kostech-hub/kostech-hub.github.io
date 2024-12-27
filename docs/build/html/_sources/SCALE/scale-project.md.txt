# SCALE.project

## Basic concepts

### Systems Engineering in the Automotive Industry

시스템 엔지니어링은 제품 개발, 특히 주문자 상표 부착 생산업체(OEM)에서 중추적인 역할을 담당합니다. 시스템 엔지니어링은 전체 수명 주기 동안 복잡한 시스템을 설계, 통합 및 관리하는 데 중점을 둔 총체적이고 학제적인 접근 방식입니다.

새로운 제품을 설계하든 단일 제품 구성 요소를 수정하든 시스템 엔지니어링은 다양한 requirements의 균형을 맞추고 여러 관점에서 프로젝트를 보기 위해 노력합니다. 고객이 원하고 기대하는 기능은 무엇인가요? 어떤 안전 및 규정 준수 표준을 충족해야 하는가? 생산은 언제 시작될 예정인가요?

### Test cases

안전 및 규정 준수 표준에 대해 자세히 살펴봅시다. 자동차를 설계하면서 충돌 안전성을 테스트하고 싶다고 가정해 보겠습니다. 구체적으로 시속 56km로 단단한 장벽에 충돌했을 때 자동차가 어떻게 작동하는지 알고 싶다고 가정해 보겠습니다. 테스트 케이스는 충돌 테스트를 설정하는 방법과 충돌 테스트가 수행되는 조건(예: 장벽, 속도, 온도 및 충격 각도)을 정의합니다.

충돌 테스트가 진행되는 동안 센서와 장치는 더미가 받는 손상 정도를 측정합니다. 예를 들어 충돌 시 운전자의 가슴이 얼마나 휘어지는지 또는 운전자의 대퇴골에 가해지는 힘의 양을 측정할 수 있습니다. 가슴 편향과 대퇴골 힘과 같은 각 측면을 requirements이라고 하며, 허용되는 값의 범위와 허용되지 않는 값의 범위가 있습니다.

### Requirements

requirements은 단독으로 존재하지 않습니다. 오히려 특정 테스트 사례와 관련하여 정의됩니다. 예를 들어 시속 56km/h 정면 충돌 테스트에서 가슴 편향값은 허용 범위 내에 있어야 합니다. 제품 개발의 일부는 향후 제품이 충족해야 하는 requirements을 정의하는 것입니다.

![alt text](images/requirements-their-thresholds.png)

### Assessment

충돌 테스트 중에 각 요건이 측정되고 값을 받습니다. 예를 들어 충돌 테스트 더미의 가슴이 46mm 휘어진 경우 이 값이 requirements의 현재 상태로 저장됩니다.

그런 다음 현재 상태를 허용 가능한 값과 허용되지 않는 값의 범위와 비교하여 실제 값이 목표 값과 얼마나 다른지 확인할 수 있습니다. 프로젝트 관리자는 언제든지 테스트 케이스를 보고 얼마나 많은 requirements이 충족되었는지 확인할 수 있습니다.

## Initial configuration

:::{note}
관리자와 같이 포괄적인 권한을 가진 사람이 처음에 ![alt text](images/project-icon.png){class="intxt-image"}**Project**를 구성해야 합니다. 이 사람은 속성, requirements 및 테스트 케이스와 같은 마스터 데이터를 만들고 수정할 수 있는 권한이 있어야 합니다. 이 초기 구성이 완료되면 관리자는 프로젝트 관리자 및 프로젝트 기여자를 위한 계정 등 추가 사용자 계정을 만들 수 있습니다.
:::

초기 구성은 예를 들어 다음과 같은 순서로 완료 할 수 있습니다.

- [Create MDM attributes](#create-mdm-attributes)
- [Create MDM requirements based on these attributes](#create-mdm-requirements-based-on-these-attributes)
- [Group the requirements into MDM test cases](#group-the-requirements-into-mdm-test-cases)
- [Create other use accounts and grant permissions](#create-other-user-accounts-and-grant-permissions)

### Create MDM attributes

1. **Configuration > MDM > Attributes**로 이동합니다.
2. 상단 오른쪽에 **New**를 클릭하면 새로운 window가 나타납니다.
3. 필요에 따라 설정을 구성합니다.
4. ![alt text](images/save-icon.png)를 클릭해서 설정을 저장합니다.

MDM attributes에 대한 자세한 지침과 각 설정에 대한 설명은 [여기](#mdm-attributes)에서 확인할 수 있습니다.

### Create MDM requirements based on these attributes

1. **Configuration > MDM > Requirements**로 이동합니다.
2. **New**를 클릭합니다.
3. 필요에 따라 설정을 구성합니다.
4. ![alt text](images/save-icon.png)를 클릭해서 설정을 저장합니다.

MDM requirements에 대한 자세한 지침과 각 설정에 대한 설명은 [여기](#mdm-requirements)에서 확인할 수 있습니다.

### Group the requirements into MDM test cases

1. **Configuration > MDM > Test cases**로 이동합니다.
2. **New**를 클릭합니다.
3. 테스트 케이스에 대한 정보를 추가하고 테스트 케이스에 포함해야 하는 requirements를 선택합니다.
4. ![alt text](images/save-icon.png)를 클릭해서 설정을 저장합니다.

MDM test cases 구성에 대한 자세한 지침과 각 설정에 대한 설명은 [여기](#mdm-test-cases)에서 확인할 수 있습니다.

### Create other user accounts and grant permissions

1. **Configuration > User Management > Users**로 이동합니다.
2. **New**를 클릭합니다.
3. 필요에 따라 설정을 구성합니다.
4. ![alt text](images/save-icon.png)를 클릭해서 설정을 저장합니다.

MDM user accounts 구성에 대한 자세한 지침과 각 설정에 대한 설명은 [여기](#user-management)에서 확인할 수 있습니다.

## Set up a project

:::{admonition} Project managers set up the project
:class: note
Project는 처음에 project 설정을 추가, 변경 및 삭제할 수 있는 권한이 있는 사용자(예: project 관리자)가 설정합니다. project가 설정되면 project 관리자는 project에 다른 멤버를 추가할 수 있습니다.
:::

예를 들어 다음과 같은 순서로 프로젝트를 설정할 수 있습니다.

- [Create a new project](#create-a-new-project)
- [Open an existing project](#open-an-existing-project)
- [Star favorite projects](#star-favorite-projects)
- [Edit a project's name or description](#edit-a-projects-name-or-description)
- [Manage project documents](#manage-project-documents)
- [Add project attributes](#add-project-attributes)

### Create a new project

1. ![](images/project-icon.png){class="intxt-image"}**Project**를 열어 projects의 overview를 표시합니다.
2. 상단 오른쪽에 **New Project**를 클릭합니다.
3. 생성할 project의 이름(Name)과 설명란(description)을 작성합니다. 
4. Project 유형(type)을 드롭 다운 메뉴에서 선택합니다.
5. **Create Project**를 클릭합니다. project는 overview에 표시되고 다시 편집할 수 있습니다. 예를 들어 생성된 project에 이제 문서(documents), 속성(attributes), 마일스톤(milestones), 요구조건(requirements) 그리고 멤버들(members)을 추가할 수 있습니다.

![alt text](images/new-project.png)

### Open an existing project

1. ![](images/project-icon.png){class="intxt-image"}**Project**를 열어 projects의 overview를 표시합니다.
2. 선택사항으로 오른쪽 상단 모서리의 **Filter by name** 필드에 project 이름을 입력하거나 다음 예정된 마일스톤을 기준으로 project를 정렬할 수 있습니다. 이러한 옵션을 사용하면 원하는 project를 빠르게 찾을 수 있습니다.
3. 목록에서 project의 이름을 클릭합니다. project가 열리고 왼쪽 사이드바에서 **Overview**가 자동으로 선택됩니다.

### Star favorite projects

1. Project를 즐겨찾기 기능처럼 선호하는 주 project를 설정 할 수 있습니다.
2. Project를 열어 즐겨찾기 할 project의 ![alt text](images/star-icon.png)**Star** 마크를 클릭합니다. 
3. 즐겨찾기된 project는 상단 메뉴에서 Projects를 선택하면 나타나는 리스트 메뉴의 Starred Projects에 표시됩니다.
4. 다시 ![alt text](images/star-icon.png)**Star** 마크를 클릭하면 즐겨찾기를 해제할 수 있습니다.

### Edit a project's name or description

1. Project를 열어 왼쪽 사이드바(sidebar)에서 **Settings**를 클릭합니다.
2. Project 이름, 유형, 설명 및 이미지를 편집합니다.
3. ![](images/save-icon.png)를 클릭하여 변경된 사항을 저장합니다.

### Manage project documents

1. Project를 엽니다. **Overview**는 자동으로 왼쪽 사이드바에서 선택됩니다.
2. **Documents** 섹션(section)을 찾습니다. 이곳에서 project 관련 문서를 관리합니다. 문서의 이름과 파일 형식, 문서를 추가한 사용자의 이름이 표 형식의 개요(overview)에 표시됩니다.

![alt text](images/project-documents.png)

### Add project attributes

프로젝트 속성(attribues)은 키-값 쌍(key-value pairs)을 사용하여 프로젝트 속성에 대한 기술적 설명을 가능하게 합니다. 이 정보를 통해 프로젝트를 분류하고 향후 관련 프로젝트 requirements을 파악할 수 있습니다.

1. 자신의 프로젝트를 엽니다.
2. 왼쪽 사이드바(sidebar)에서 **Attributes**를 클릭합니다.
3. **Edit**를 눌러 새 창을 띄웁니다.
4. ![alt text](images/black-plus.png){class="intxt-image"}를 눌러 새 라인을 추가합니다.
5. 왼쪽에 위치한 영역(field)에 속성(attribute)의 이름을 입력합니다. 해당 영역(field)는 자동완성 기능을 가지고 있습니다. 입력할 때 과거에 입력했던 항목들에서 예측해 표시해줍니다.
6. 오른쪽에 위치한 드롭-다운(drop-down) 리스트에서 하나 혹은 두개 이상의 값들을 선택합니다.
7. **Save**를 클릭하여 속성들을 업데이트 합니다.

![alt text](images/add-project-attributes.png)

:::{admonition} Configure MDM attributes in advance
:class: tip
MDM 속성들은 프로젝트에 추가하기 전에 **Configuration > MDM > Attributes에서 구성되어야 합니다. 이 초기 구성은 MDM 권한이 있는 사용자(ex. admin)가 수행합니다.
:::

### Milestones

#### Add project milestones

1. 자신의 프로젝트를 엽니다. 왼쪽 사이드바(sidebar)에서 **Overview**가 자동으로 선택됩니다.
2. **Milestones** 섹션을 찾아 ![](images/black-plus.png){class="intxt-image"}를 클릭하여 새 창을 표시합니다.
3. (**A**)에 이름과 (**B**)에 설명(description)을 입력합니다. 
4. 하나의 단일 계획(plan)은 master(**C**)로 지정하여 가장 관련성이 높은 프로젝트 마일스톤이 포함되어 있음을 나타낼 수 있습니다. 마스터 계획은 시간 스케일(time scale)과 목록에서 가장 먼저 표시됩니다. 그리고 글꼴과 아이콘으로 강조 표시됩니다.
5. 일정에 마일스톤을 원하는 수만큼 추가합니다. 각 마일스톤에 이름, 날짜, 설명을 입력합니다.(**D**)
6. **Save** (**H**)를 클릭하여 마일스톤 계획을 업데이트 합니다.

![alt text](images/add-project-milestones.png)

#### View milestones in the overview

1. 자신의 프로젝트를 엽니다. **Overview**가 왼쪽 사이드바(sidebar)에서 자동으로 선택됩니다.
2. **Milesones** 섹션에서 모들 프로젝트 참가자들에 대한 프로젝트 일정의 개요를 확인할 수 있습니다.

![alt text](images/project-milestones.png)

- **A**: 시간 스케일(time scale)의 그래픽 표현
- **B**: 마일스톤에 마우스를 위치 시켰을 때 마일스톤에 대한 상세 정보가 표시됩니다.
- **C**: 현재 날짜가 표시되며 수식선과 연결됩니다.
- **D**: 네 가지 옵션이 표시됩니다.
    - ![alt text](images/download-plot-icon.png){class="intxt-image"}: Download plot as a .png
    - ![alt text](images/zoom-in-icon.png){class="intxt-image"}: Zoom in
    - ![alt text](images/zoom-out-icon.png){class="intxt-image"}: Zoom out
    - ![alt text](images/reset-axes-icon.png){class="intxt-image"}: Reset axes
- **E**: List of schedules: 시간 척도(time scale)의 그래픽 표현 아래에는 마일스톤 계획별로 정렬된 일정이 표시되며, 이를 펼치거나 접을 수 있습니다. 마일스톤 이름, 설명 및 날짜는 표 형식의 개요로 표시됩니다.
- **F**: 존재하는 마일스톤 계획을 편집하기 위해 **Edit**을 클릭합니다.
- **G**: 새 마일스톤 계획을 추가하기 위해 ![](images/black-plus.png){class="intxt-image"}를 클릭합니다.이 아이콘의 표시는 사용자의 권한에 맞추어 표시됩니다.

#### Add requirements and test cases to the project

Requirements는 테스트 케이스(test cases)를 통해 프로젝트에 추가됩니다. 즉, 프로젝트에 테스트 케이스를 추가하면 해당 테스트 케이스에 포함된 모든 requirements도 자동으로 추가됩니다.

1. 프로젝트를 엽니다.
2. 왼쪽 사이드바(sidebar)에서 **Requirements**를 클릭합니다.
3. 상단 오른쪽에 **Add**를 클릭합니다. **Add MDM Test Cases to Project 영역이 표시됩니다.
4. 적절한 테스트 케이스 (![alt text](images/check-box-icon.png){class="intxt-image"})를 선택합니다.
5. ![](images/save-icon.png){class="intxt-image"}를 클릭하면 테스트 케이스(test cases)에 포함된 모든 requirements가 자신의 프로젝트의 추가됩니다.

![alt text](images/add-mdm-requirements-to-project.png)

:::{admonition} Requirements and test cases can be edited to make them project-specific
:class: tip
특정 프로젝트 내의 requirements 및 테스트 케이스(test cases)를 project requirements 및 project test cases라고 합니다. 이는 MDM requirements 및 MDM test cases에서 파생됩니다. 이 과정에서 모든 속성, 임계값 등이 복사되며 필요한 경우 추가로 변경할 수 있습니다.
:::

### Add project members

1. 자신의 프로젝트를 엽니다.
2. 왼쪽 사이드바(sidebar)에서 **Project members를 클릭합니다. 여기에서 프로젝트 접근 권환이 있는 모든 사용자들을 확인할 수 있습니다.
3. 상단 오른쪽의 **+ADD**를 클릭하여 프로젝트에 새 멤버를 추가합니다. 새 창이 표시됩니다.
4. 상단에 프로젝트에 추가할 사용자를 선택합니다. 사용자 이름으로 사용자들을 찾을 수 있으며 이름 및 이메일 주소로 표시됩니다.
5. 하단에 사용자에 활당된 역할(role)을 선택합니다.
6. 향후에 사용자의 role을 변경할 필요가 있을 경우 **Project role** 열의 role을 더블 클릭하여 변경할 수 있습니다.

![alt text](images/add-new-project-member.png)

:::{admonition} Create user accounts and project roles in advance
:class: tip
- 사용자를 프로젝트에 추가하려면 먼저 **Configuration > User Management > Users**에서 사용자를 구성해야 합니다. 이 초기 구성은 해당 권한이 있는 사용자(예: admin)가 수행합니다.
- 프로젝트 role은 **Configuration > User Management > Project roles**에서 구성해야 사용자에게 할당할 수 있습니다. 이 초기 구성은 해당 권한이 있는 사용자(예: admin)가 수행합니다.
:::

## Tailor requirements to be project-specific

:::{admonition} Project managers nad/or contributors can tailor requirements
:class: note
프로젝트 관리자와 프로젝트 기여자 모두 프로젝트에 맞게 MDM requirements를 조정할 수 있습니다.

- **MDM requirements**: **Configuration** > **MDM** > **Requirements** 아래의 requirements를 MDM requirements라고 합니다. requirements template 또는 SCALE.sdm 애플리케이션에 대한 global requirements 데이터베이스라고 생각할 수 있습니다.

- **Project requirements**: 특정 프로젝트 내의 requirements를 project requirements이라고 합니다. 프로젝트 requirements은 MDM requirements에서 파생됩니다. 이 과정에서 원래 requirements의 속성, 임계값 등이 프로젝트별 requirements로 복사되며 필요한 경우 추가로 변경할 수 있습니다. 프로젝트에는 동일한 MDM requirements에서 파생된 여러 프로젝트 requirements이 있을 수 있습니다.
:::

예를 들어 다음과 같은 순서로 프로젝트를 맞춤 설정 할 수 있습니다.

- [View a requirement's details](#view-a-requirements-details)
- [Edit a test case to be project-specific](#edit-a-test-case-to-be-project-specific)
- [Edit the requirements to be project-specific](#edit-the-requirements-to-be-project-specific)

### Open an existing project

1. ![](images/project-icon.png){class="intxt-image"}**Project**를 열어 프로젝트의 overview를 표시합니다.
2. 오른쪽 상단 모서리의 이름으로 필터링 필드에 프로젝트 이름을 입력하거나 다음 예정된 마일스톤을 기준으로 프로젝트를 정렬할 수 있습니다. 이러한 옵션을 사용하면 원하는 프로젝트를 빠르게 찾을 수 있습니다.
3. 목록에서 프로젝트 이름을 클릭합니다. 프로젝트가 열리고 왼쪽 사이드바에서 overview가 자동으로 선택됩니다.

### View a requirement's details

1. 프로젝트를 엽니다.
2. 왼쪽 사이드바(sidebar)에서 requirements를 클릭합니다. 여기에 프로젝트 requirements의 overview가 표시됩니다. 필요에 따라 이 개요에서 requirements을 필터링하거나 그룹화할 수 있습니다.
3. requirements를 클릭한 다음 requirements에 대한 자세한 정보를 보려면 requirement를 클릭합니다.

### Edit a test case to be project-specific

1. 프로젝트를 엽니다.
2. 왼쪽 사이드바에서 **Requirements**을 클릭합니다.
3. Overview에서 requirement를 마우스 오른쪽 버튼으로 클릭합니다. 컨텍스트 메뉴가 열립니다.
4. **Edit test case [Name of test case]**을 클릭합니다. 새 창이 열립니다.
5. 테스트 케이스가 프로젝트에 맞게 수정합니다.
6. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다.

테스트 케이스 설정에 대한 자세한 지침은 MDM test cases 페이지에서 확인할 수 있습니다.

![alt text](images/edit-a-project-test-case.png)

### Edit the requirements to be project-specific

한번에 하나의 requirement를 편집하거나 여러 requirements를 동시에 편집할 수 있습니다. 

#### Edit one requirement to be project-specific

1. 자신의 프로젝트를 엽니다.
2. 왼쪽 사이드바에서 **Requirements**을 클릭합니다.
3. Overview에서 requirements를 마우스 오른쪽 버튼으로 클릭합니다. 컨텍스트 메뉴가 열립니다.
4. **Edit requirement**을 클릭합니다. 새 창이 열립니다.
5. requirements를 프로젝트별로 수정합니다.
6. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다.

requirement 설정에 대한 자세한 지침은 MDM requirements 페이지에서 확인할 수 있습니다.

![alt text](images/edit-a-project-requirement.png)

#### Eidt multiple requirements at ones

1. 프로젝트를 엽니다.
2. 왼쪽 사이드바에서 **Requirements**을 클릭합니다.
3. 여러 requirements를 선택한 다음(Ctrl. + 클릭) 마우스 오른쪽 버튼을 클릭합니다. 컨텍스트 메뉴가 열립니다.
4. **Edit requirements**을 클릭합니다. 새 창이 열립니다. 여기에서 선택한 모든 requirements의 이름, 설명 및 평가 임계값(thresholds)을 동시에 편집할 수 있습니다.

##### Edit the names

1. 상단 박스를 선택합니다.
2. 첫번째 드롭-다운 리스트에서 **Change to apply**에서 옵션을 선택합니다.
    - **Replace**: requirement 이름 내에서 특정 단어 하나를 변경합니다.
    - **Replace all**: 전체 requirement 이름을 변경합니다.
    - **Add to beginning**: requirement 이름의 시작 부분에 특정 텍스트를 추가합니다.
    - **Add to end**: requirement 이름 끝에 특정 텍스트를 추가합니다.
3. 텍스트 영역(text filed)에 자신의 텍스트를 입력합니다.
4. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다.

![alt text](images/correct-a-typo-in-both-requirement-names.png)

##### Edit the descriptions

1. 중간 박스를 선택합니다.
2. **Description**에 텍스트를 입력합니다.
3. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다.

![alt text](update-the-descriptions-of-both-requirements.png)

##### Edit the assessment thresholds

1. **Apply Changes to all Assessments** 영역을 펼칩니다.
2. 아래쪽 상자를 선택합니다.
3. 필요에 따라 평가 임계값(assessment thresholds)을 수정합니다. 자세한 지침은 MDM requirements 페이지에서 확인할 수 있습니다.
4. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다.

## Configure the requirements grid

:::{admonition} Project managers and/or contributors can configure the grid
:class: note
프로젝트 관리자와 프로젝트 기여자 모두 열을 재정렬하고 필터를 적용하는 등 requirements grid를 구성할 수 있습니다.
:::

Requirements grid는 예를 들어 다음과 같은 순서로 구성할 수 있습니다.

- [Toggle and rearrange the columns](#toggle-and-rearrange-the-columns)
- [Group requirements by column headers](#group-requirements-by-column-headers)
- [Apply column filters](#apply-column-filters)
- [Change the sorting order](#change-the-sorting-order)
- [Save the configuration as a view](#save-your-configuration-as-a-view)
- [Share views with other users](#share-views-with-other-users)

### Basic concept

Grid의 각 줄은 하나의 requirement(**B**)을 나타내고, 각 열은 requirement(**A**)에 대한 하나의 정보를 나타냅니다. 때로는 일부 열만 표시하고 다른 열은 숨기는 것이 도움이 될 수 있습니다. 필요에 따라 grid를 사용자 지정할 수 있습니다.

![alt text](images/requirements-grid-and-columns.png)

Grid 구성을 완료한 후에는 구성(configuration)을 'View'라는 이름으로 저장하고 이 view를 다른 사용자와 공유할 수도 있습니다. 이렇게 하면 나중에 구성에 다시 액세스할 수 있습니다. 예시: 서로 다른 두 개의 views를 만들 수 있습니다. 각 view에는 특정 작업에 필요한 열만 포함됩니다. 작업을 수행할 때 적절한 view를 선택하기만 하면 됩니다.

:::{admonition} What does the view define?
:class: tip
View는 레이아웃(layout)의 다음 측면을 제어합니다.

- 표시될 열
- 열이 표시되는 순서
- 열을 그룹화할지에 대한 여부
- 필터 적용 여부
- 열 내용을 오름차준 또는 내림차순으로 표시할지 여부

Note: View는 열의 크기를 제어하지 않습니다.
:::

:::{admonition} What does the view define?
:class: tip
SCALE.sdm에는 여러가지 grid가 있습니다. 예를 들어, ![](images/project-icon.png){class="intxt-image"}**Project**에는 requirements grid가 있고 **Configuration** > **MDM** > **Requirements** 아래에 grid가 있습니다. 각 grid는 개별적으로 구성해야 합니다. View는 모든 grid에 저장되지 않습니다. 
:::

### Toggle and rearrange the columns

1. 프로젝트를 엽니다.
2. **Requirements**를 클릭합니다.
3. grid의 오른쪽 사이드의 ![alt text](images/grid-icon.png){class="intxt-image"}를 클릭하면 사이드바가 표시됩니다.
4. 표시할 열을 선택하여 체크 표시(![](images/red-check-box.png){class="intxt-image"})가 되도록 합니다.
5. Optional: 마우스 커서를 ![alt text](images/move-icon.png){class="intxt-image"}에 가져가면 커서가 ![alt text](images/hand-icon.png){class="intxt-image"}로 바뀌며 드래그 하여 그리드에서 열의 순서를 바꿀 수 있습니다.

![alt text](images/configure-the-grid.png)

### Group requirements by column headers

1. 프로젝트를 엽니다.
2. **Requriements**를 클릭합니다.
3. 마우스 커서를 열의 헤더(header)에 위치시키면 커서가 ![alt text](images/pointing-hand-icon.png){class="intxt-image"}로 바뀝니다.
4. 열의 헤더를 드래그 하여 그리드 상단의 **Drag hear to set row groups**로 드롭합니다. 데이터들은 해당 열에 의해 그룹화 되어 표시됩니다.
5. 필요에 따라 다른 열에 대해서도 같은 방법으로 그룹화 할 수 있습니다.

![alt text](images/group-requirements-by-column-headers.png)

:::{admonition} Alternative to drag & drop
:class: tip
다음고 같이 열 헤더에 의한 그룹화를 진행 할 수 있습니다.

1. 프로젝트를 엽니다. 
2. **Requirements**를 클릭합니다.
3. 마우스 커서를 ![](images/column-mark.png){class="intxt-image"} 위로 위치시키고 클릭하여 컨텍스트 메뉴를 표시합니다.
4. **Group by [column name]** 옵션을 선택합니다. Grid에서 데이터는 해당 열에 의해 그룹화 됩니다.
5. 필요에 따라 다른 열에 대해서도 같은 방법으로 그룹화 할 수 있습니다.
:::

### Apply column filters

1. 프로젝트를 엽니다.
2. **Requirements**를 클릭합니다.
3. 열 헤더(header) 바로 아래 줄에 텍스트를 입력합니다.
4. 선택 사항으로 추가 필터 옵션에 액세스하려면 ![alt text](images/filter-icon.png){class="intxt-image"}를 클릭합니다.
5. 필요한 경우 같은 방법으로 다른 열에도 필터를 적용합니다.

![alt text](images/apply-column-filters.png)

### Change the sorting order

1. 프로젝트를 엽니다.
2. 왼쪽 사이드바에서 **Requirements**을 클릭합니다.
3. 오름차순으로 정렬하려면 열 헤더를 클릭합니다.
4. 내림차순으로 정렬하려면 두 번 클릭합니다.
5. 정렬을 제거하려면 세 번 클릭합니다.

### Sort multiple columns

여러 열을 기준으로 정렬할 수도 있습니다. 예를 들어, 먼저 대상 시장(target market)별로 requirements를 정렬할 수 있습니다. 그런 다음 여러 requirements가 동일한 시장에 적용되는 경우 알파벳 순서로 정렬할 수 있습니다.

1. 프로젝트를 엽니다.
2. 왼쪽 사이드바에서 requirements를 클릭합니다.
3. 열 헤더를 클릭하여 데이터를 정렬합니다. 예를 들어, 대상 시장별로 requirements를 정렬합니다.
4. Shift 키를 누른 상태에서 다른 열 머리글을 클릭하여 두 번째 수준별로 정렬합니다. 예를 들어 동일한 시장에 여러 requirements가 적용되는 경우 이름별로 알파벳순으로 정렬할 수 있습니다. 참고: 열 레이블 오른쪽에 표시되는 숫자는 정렬이 적용되는 순서를 나타냅니다. 이를 통해 여러 열에서 정렬 순서를 이해하는 데 도움이 됩니다.
5. 필요한 경우 Shift 키를 누른 상태에서 추가 열 헤더을 계속 클릭합니다.

![alt text](images/sort-multiple-columns-in-project.png)

### Save your configuration as a view

1. 프로젝트를 엽니다.
2. **Requirements**를 클릭합니다.
3. Grid 상단 오른족의 ![](images/grid-icon.png){class="intxt-image"}를 클릭하고 사이드 바를 표시합니다.
4. ![alt text](images/views-setting-icon.png){class="intxt-image"} **Views**를 클릭합니다. 존재하는 모든 뷰(view)가 리스트로 표시됩니다.
5. ![alt text](images/plus-only-icon.png){class="intxt-image"} **New View**를 클릭합니다.
6. 뷰(view)에 대한 이름을 입력하고 **Save**를 클릭합니다. 자신의 view가 리시트에 추가됩니다.

:::{admonition} What is the default view?
:class: tip
Views 목록에는 기본값(default)이라는 항목이 있습니다. 아직 사용자 지정 보기(views)를 구성하지 않은 경우 기본 보기(default views)가 사용됩니다. 글로벌 관리자만 기본 보기를 만들거나 수정할 수 있습니다. 일반 사용자는 이 보기를 편집할 수 없습니다.
:::

![alt text](images/save-your-configuration-as-a-view.png)

### Share views with other users

다른 사용자와 보기(views)를 공유할 수 있습니다. 예를 들어 관리자는 여러 개의 서로 다른 보기를 만들 수 있습니다. 각 보기에는 특정 작업을 수행하는 데 도움이 되는 열과 필터가 포함되어 있습니다. 그런 다음 관리자는 이러한 보기를 해당 작업을 담당하는 동료들과 공유할 수 있습니다.

1. 프로젝트를 엽니다.
2. 왼쪽 사이드바에서 **Requirements**을 클릭합니다.
3. Grid의 맨 오른쪽의 ![](images/grid-icon.png){class="intxt-image"} 클릭합니다. 사이드 바가 표시됩니다.
4. ![](images/views-setting-icon.png) **Views**를 클릭합니다. 여기에 모든 기존 뷰(views) 목록이 표시됩니다.
5. 보기에 대한 추가 옵션을 보려면 ![alt text](images/vertical-three-dot.png)를 클릭합니다.
6. ![alt text](images/share-icon.png) **Share**를 클릭합니다. 팝업 창이 열립니다.
7. 드롭다운 목록에서 분야(discipline)를 선택합니다.
8. ![](images/confirm-icon.png) **Confirm**을 클릭합니다. view가 해당 분야(discipline)의 모든 사용자와 공유됩니다.

## Report the current requirement status

:::{admonition} Project contributors can save the requirement staus
:class: note
일반적으로 프로젝트 기여자(project contributors)는 프로젝트 requirement의 상태를 저장합니다. 상태는 특정 시점의 실제 값을 나타냅니다. 이 값에는 코멘트나 첨부 파일과 같은 선택적 속성이 첨부될 수 있습니다. 이 값은 기존 임계값(thresholds)과 비교되며 결과에 따라 빨간색, 노란색 또는 녹색과 같은 특정 색상으로 표시됩니다.
:::

Requirement 상태는 예를 들어 다음과 같은 순서로 저장할 수 있습니다.

- [View the status of a requirement](#view-the-status-of-a-requirement)
- [Report a new status](#report-a-new)
- [Monitor project status over time](#monitor-project-status-over-time)

### Open an existing project

1. ![](images/project-icon.png){class="intxt-image"}**Project**를 엽니다.
2. 선택사항 : **Filter by name**에 프로젝트 이름을 입력하거나 다음 예정된 마일스톤을 기준으로 프로젝트를 정렬할 수 있습니다. 
3. 리스트의 프로젝트 이름을 클릭합니다. 선택한 프로젝트가 열리면서 왼쪽 사이드바의 **Overview**가 자동으로 선택됩니다.

### View the status of a requirement

Requirement의 상태를 확인하는 다음과 같은 방법들이 있습니다.

- [View the status of one single requirement](#view-the-status-of-one-single-requirement)
- [View the status of a requirement group](#view-the-status-of-requirement-groups)
- [View aggregated statuses in the sidebar](#view-aggregated-statuses-in-the-sidebar)

#### View the status of one single requirement

1. 프로젝트를 엽니다.
2. 왼쪽 사이드바에서 **Requirements**를 클릭합니다. 여기에서 프로젝트 requirement의 개요를 볼 수 있습니다. 필요에 따라 이 개요에서 requirement을 필터링하거나 그룹화할 수 있습니다.
3. Requirement를 클릭하고 ![alt text](images/two-left-arrow.png){class="intxt-image"}를 클릭하면 상세 정보를 확인할 수 있습니다.

#### View the status of requirement groups

대부분의 경우 각 requirement를 개별적으로 살펴보지 않습니다. 그보다는 테스트 케이스(test case)별로 requirement를 그룹화할 것입니다. 이 그룹화된 보기 내에서 각 그룹은 상태(예: 빨간색, 노란색 또는 녹색)를 받습니다. 이렇게 하면 어떤 그룹에 더 많은 주의가 필요한지 즉시 파악할 수 있습니다.

1. 프로젝트를 엽니다.
2. 왼쪽 사이드바에서 **Requirements**를 클릭합니다.
3. 하나 이상의 열 헤더(column header)를 기준으로 requirement을 그룹화합니다.
4. 그룹을 확장하면 각 개별 requirement의 상태(예: 빨간색, 노란색 또는 녹색)가 표시되고 그룹에도 상태가 표시됩니다. 그룹의 상태는 집계됩니다. 즉, 그룹은 자동으로 최악(worst)의 상태를 상속받습니다.

예제 이미지에서 그룹에는 녹색 requirement 3개, 노란색 requirement 5개, 빨간색 requirement(B) 1개가 포함되어 있습니다. 빨간색 상태는 그룹 내에서 가장 나쁜 상태이므로 그룹은 자동으로 빨간색 상태(A)를 상속합니다.

![alt text](images/group-status-aggregated.png)

:::{admonition} Notes about the group status
:class: note
- 일부 그룹에는 ![alt text](images/hand-star-icon.png){class="intxt-image"}가 표시됩니다. 이는 그룹에 평가 색상이 수동으로 선택된 requirements이 하나 이상 포함되어 있음을 의미합니다.
- 공개(public) 및 비공개(private) 상태가 모두 집계됩니다. 즉, 그룹은 공개 또는 비공개 여부에 관계없이 자동으로 최악의(worst)의 상태를 상속받게 됩니다. 
:::

#### View aggregated statuses in the sidebar

1. 프로젝트를 엽니다.
2. **Requirements**를 클릭합니다. 여기에 프로젝트 requirements의 overview가 표시됩니다. 필요에 따라 이 개요에서 requirements을 필터링하거나 그룹화할 수 있습니다.
3. 여러 requirements을 선택한 다음(Ctrl. + 클릭) **<<** 클릭하면 이러한 requirements의 집계된 상태를 볼 수 있습니다. 프로젝트 상태 요약(overview)이 사이드바에 표시됩니다.

- 선택한 프로젝트 requirements의 수 및 집계된(aggregated) 상태
- 다양한 상태의 수와 비율을 보여주는 막대형 차트

![alt text](images/sidebar-view-with-mutiple-selection.png)

### Manually report the status

프로젝트 requirements의 상태를 보고할 수 있습니다. 상태는 특정 시점의 실제 값을 나타냅니다. 이 값은 코멘트나 첨부 파일과 같은 선택적 속성과 함께 표시될 수 있습니다. 이 값은 기존 임계값과 비교되며 결과에 따라 빨간색, 노란색 또는 녹색과 같은 특정 색상으로 표시됩니다.

팁: 다양한 requirements의 상태를 보고해야 하는 경우에는 먼저 필요에 맞게 특별히 맞춤화된 보기를 만드는 것이 좋습니다.

1. 프로젝트를 엽니다.
2. **Requirements**를 클립합니다. 여기에서 프로젝트 requirements의 개요를 볼 수 있습니다. 필요에 따라 이 개요에서 requirements을 필터링하거나 그룹화할 수 있습니다.
3. requirement(예: 'chest deflection')을 클릭한 다음 **<<**에서 requirement에 대한 자세한 정보를 확인합니다.
4. **Report Status** 버튼을 클릭합니다. 화면이 변경됩니다. 
5. 상태에 대한 값을 입력합니다. 예를 들어 충돌 테스트 더미의 가슴이 -46mm 휘어진 경우 이 값을 requirement의 현재 상태로 입력합니다. 평가 원(assessment circle)이 자동으로 색상이 변경되어 해당 값이 requirement의 임계값과 어떻게 일치하는지 보여줍니다.
6. Optional: 자동 평가(assessment)를 수동으로 재정의하려면 평가 원(assessment circle)을 클릭하고 다른 색상을 선택합니다. 참고사항으로 수동으로 선택한 평가는 requirements 그리드에서 기호로 표시됩니다.
7. Optional: **Add Files**를 클릭하여 관련 문서 또는 보고서를 첨부합니다.
8. **Save Private** 또는 **Save Public**을 클릭하여 상태를 저장합니다. 비공개(private) 및 공개(public) 상태에 대한 자세한 내용은 아래에서 확인할 수 있습니다.

:::{admonition} Requirements without numerical values
:class: tip
위의 지침은 requirement의 상태를 숫자 값으로 저장하는 방법을 알려줍니다(예: -46mm의 가슴 처짐). 그러나 일부 requirement에는 숫자 값이 없습니다. 대신 "예" 또는 "아니오"와 같은 가능한 옵션 목록에서 값을 가져옵니다. 이러한 requirement의 상태를 저장하는 것도 가능합니다. 유일한 차이점은 숫자 값을 입력하는 대신 드롭다운 목록에서 값을 선택한다는 것입니다.
:::

### Change a status from private to public

1. 프로젝트를 엽니다.
2. 왼쪽 사이드바에서 **Requirements**을 클릭합니다. 여기에 프로젝트 requirements의 개요(overview)가 표시됩니다. 필요에 따라 이 개요에서 requirements을 필터링하거나 그룹화할 수 있습니다.
3. requirement을 마우스 오른쪽 버튼으로 클릭하여 컨텍스트 메뉴를 표시합니다.
4. **Set public**을 클릭합니다. 비공개(private) 항목이 공개(public)로 표시되는 즉시 항목의 타임스탬프(timestamp)가 현재 시간으로 설정됩니다.

:::{admonition} Private entries vs. public entries
:class: tip
비공개(Private) 항목:

- 생성한 사용자만 볼 수 있음
- 편집 및 삭제 가능
- requirement와 user에 대해서 한 번만 존재할 수 있습니다. 즉, 동일한 요건에 대해 다른 비공개(private) 상태를 보고(report)하면 기존 상태를 덮어쓰게 됩니다. 기존 상태를 덮어쓰지 않으려면 동일한 요건에 대한 다른 비공개(private) 항목을 보고(report)하기 전에 해당 상태를 공개(public)로 설정하세요.

공개(Public) 항목

- requirement에 접근할 수 있는 모든 사용자가 볼 수 있습니다.
- 사용자에 관계없이 편집하거나 삭제할 수 없습니다.
:::

### Monitor project status over time

시간 경과에 따른 프로젝트의 상태를 추적할 수 있습니다. 즉, 프로젝트의 현재 상태를 이전 날짜의 상태와 비교할 수 있습니다. 예를 들어, 특정 requirement을 살펴보고 그 값이 한 마일스톤에서 다음 마일스톤으로 어떻게 변경되었는지 확인할 수 있습니다.

1. 프로젝트를 엽니다.
2. 왼쪽 사이드바에서 **Requirements**를 클릭합니다.
3. 마일스톤을 클릭하여 영역을 확장합니다. 여기에는 마스터(master)로 설정된 마일스톤 계획만 표시됩니다. 계획이 표시되지 않으면 계획이 마스터로 활성화되어 있는지 확인하세요.
4. Optional: ** + More schedules**를 클릭하고 필요에 따라 추가 타임라인들을 선택합니다.
5. Optional: ![alt text](images/calendar-icon.png){class="intxt-image"}를 클릭하고 캘린더(calendar)에서 날짜를 선택합니다. 또는 날짜 선택 필드에 날짜를 직접 입력합니다. 월/일/년(예: 1/31/2024)과 같은 날짜 형식을 사용합니다.
6. requirement 상태가 선택한 날짜의 값을 표시하도록 변경됩니다. 그에 따라 마일스톤 타임라인에 날짜 표시기(진한 파란색 선)가 배치됩니다.

![alt text](images/monitor-project-status-over-time.png)

## User interface

![](images/project-icon.png){class="intxt-image"}**Project**의 사용자 인터페이스는 다음의 요소들로 구성됩니다.

- **A**: 화면 상단에는 [Toolbar](#tool-bar)가 위치합니다.
- **B**: 메인 윈도우(main window)입니다. 메인 윈도우는 다음 항목들을 표시합니다.
    - 모든 프로젝트의 목록 (예 : [project selection](#project-selection))
    - 특정 프로젝트에 대한 상세 (예 : [project view](#project-view))

![alt text](images/user-interface-project.png)

### Tool bar

사용자 인터페이스(User interface) 상단에는 위치가 고정되어 있고 일반적인 애플리케이션 기능 및 메뉴가 포함된 도구 모음이 있습니다.

- [A: Project](#a-project)
- [B: Notifications](#b-notifications)
- [C: Jobs](#c-jobs)
- [D: Help](#d-help)
- [E: Burger menu](#e-burger-menu)

![alt text](images/project-toolbar.png)

#### A: Project

프로젝트에서 다음 옵션에 접근할 수 있습니다.

- ![alt text](images/dot-list-icon.png){class="intxt-image"} **All projects**: [open an existing project](#open-an-existing-project) 또는 [create a new project](#create-a-new-project)를 할 수 있습니다. 
- ![alt text](images/star-icon.png){class="intxt-image"} **Starred project**: 관심 프로젝트로 선택한 프로젝트를 직접 열 수 있습니다.
- ![alt text](images/result-icon.png){class="intxt-image"} **Result**: ![](images/project-icon.png){class="intxt-image"}에서 ![](images/result-icon.png){class="intxt-image"}로 이동할 수 있습니다.

#### B: Notifications

![alt text](images/bell-icon.png){class="intxt-image"}를 클릭하여 **Notifications**를 을 엽니다. 여기에서 공지 사항 및 작업 알림 목록을 볼 수 있습니다. [알림에 대한 자세한 정보를 확인하세요](#announcements)

#### C: Jobs

![alt text](images/jobs-icon.png){class="intxt-image"}를 클릭하여 **Jobs** 영역을 엽니다. 여기에서 add-on이나 사용자 입력에 의해 트리거되는 등 애플리케이션에서 실행 중인 작업 목록을 볼 수 있습니다. 작업 상태(보류 중, 실행 중, 성공, 실패)가 동적으로 표시됩니다. 여기에서 작업 로그 파일에 액세스하고 작업 아티팩트(artifacts)를 다운로드할 수 있습니다. [작업에 대한 자세한 정보를 확인하세요](#jobs)

#### D: Help

![alt text](images/question-icon.png){class="intxt-image"}를 클릭하면 SCALE.sdm의 매뉴얼을 확인할 수 있습니다.

#### E: Burger menu

![alt text](images/burger-menu-icon.png){class="intxt-image"}를 클릭하면 다음 옵션들에 접근할 수 있습니다.

- ![alt text](images/my-profile-icon.png){class="intxt-image"} **My profile**: 개인 설정을 엽니다. 여기에서 비밀번호를 변경하고 [access token](#access-tokens)을 관리할 수 있습니다.
- ![alt text](images/configuration-icon.png){class="intxt-image"} **Configuration**: [configuration](#configuration) 영역을 엽니다. 키(key) 사용자 또는 관리자와 같이 해당 권한이 있는 사용자는 여기에서 처음에 SCALE.sdm을 구성할 수 있습니다. 예를 들어, 마스터 데이터를 저장하고, 애드온을 설치하고, 사용자 계정을 관리할 수 있습니다.
- ![alt text](images/admin-area-icon.png){class="intxt-image"} **Admin area**: 이 항목은 [Staff](#user-management)로 지정된 사용자만 볼 수 있습니다.
- ![alt text](images/about-icon.png){class="intxt-image"} **About**: 애플리케이션에 대한 정보를 확인합니다. 여기에서 현재 설치된 버전을 확인할 수 있습니다. 애플리케이션과 관련된 오픈 소스 소프트웨어 및 라이선스에 대한 정보도 볼 수 있습니다.
- ![alt text](images/logout-icon.png){class="intxt-image"} **Logout**: 애플리케이션에서 로그아웃 합니다.

### Project selection

[tool bar](#tool-bar)에서 ![](images/dot-list-icon.png) **All projects**를 클릭하면 모든 프로젝트의 개요에 접근할 수 있습니다.

![alt text](images/projects-overview.png)

- **A**: 모든 프로젝트들의 목록
- **B**: 사용자가 관심 항목으로 등록한 모든 프로젝트들의 목록 
- **C**: 프로젝트 정보
    - 프로젝트 아이콘
    - 프로젝트 유형 / 프로젝트 이름
    - 관심 항목 등록 및 해제 아이콘
    - 현재 사용자의 프로젝트 역할
    - 우측 정렬된 항목: 다음에 예정된 마일스톤
- **D**: 새 프로젝트를 만들기 위한 버튼
- **E**: 목록에 표시될 프로젝트를 필터링 하기 위한 이름을 입력
- **F**: 프로젝트 목록을 분류하기 위한 메뉴
    - _Name_ - 프로젝트 이름의 알파벳 순서대로 정렬됩니다.
    - _Next milestone_ - 다음에 예정된 마일스톤을 기준으로 프로젝트를 시간순으로 정렬합니다.

### Project view

프로젝트 뷰(project view)의 왼쪽 사이드 바에는 다음의 다섯가지 메뉴가 있습니다.

- **A**: [Overview](#overview)
- **B**: [Attributes](#attributes)
- **C**: [Requirements](#requirements-1)
- **D**: [Settings](#settings)
- **E**: [Project members](#project-members)

**Collapse sidebar (F)**를 클릭하면 사이드바를 축소하여 각 보기에 더 많은 공간을 확보할 수 있습니다.

![alt text](images/menu-items-within-the-project-view.png)

#### Overview

프로젝트를 선택하면 개요(overview)가 자동으로 표시됩니다. 프로젝트 개요에는 다음 패널이 표시됩니다.

- **A**: [Description](#a-description)
- **B**: [Documents](#b-documents)
- **C**: [Milesontes](#c-milestones)

![alt text](images/project-overview.png)

##### A: Description

![alt text](images/project-description.png)

- **A**: 프로젝트 아이콘, 이름과 유형
- **B**: 프로젝트 설명을 위한 자유 텍스트 필드(free text field)와 일반적으로 프로젝트 범위를 포함합니다.

##### B: Documents

프로젝트 관련 문서를 관리할 수 있습니다. 문서의 이름과 파일 유형, 문서를 추가한 사용자의 이름이 표 형식의 개요에 표시됩니다.

##### C: Milestones

모든 프로젝트 참여자의 프로젝트 일정에 대한 개요를 볼 수 있습니다. [프로젝트 마일스톤에 대한 자세한 정보를 확인하세요.](#milestones)

![alt text](images/c-project-milestones.png)

#### Attributes

**Attributes** 영역에서 프로젝트에 속성을 추가할 수 있습니다. 이를 통해 프로젝트를 분류하고 향후 관련 프로젝트 requirements를 파악할 수 있습니다. [프로젝트 속성 추가에 대한 자세한 정보를 확인하세요.](#add-project-attributes)

![alt text](images/project-attributes.png)

#### Requirements

**Requirements** 영역은 다음 요소들을 포함합니다.

- [A: Milestones](#a-milestones)
- [B: Requirements grid](#b-requirements-grid)
- [C: Add button](#c-add-button)
- [D: Side panel](#d-side-panel)
    - [Status](#status)
    - [Details](#details)
    - [Thresholds](#thresholds)
    - [Context](#context)
    - [History](#history)
    - [Attachmnts](#attachments)
- [Context menu](#context-menu)

![alt text](images/project-requirements.png)

##### A: Milestones

요소(element)를 클릭하여 확장 및 축소할 수 있습니다. 기본적으로 마스터 플래그가 지정된 시간 스케줄이 표시됩니다. 선택적으로 추가 마일스톤을 표시할 수 있습니다. [requirements가 있는 마일스톤 보기에 대한 자세한 내용을 참조하세요.](#monitor-project-status-over-time)

##### B: Requirements grid

Requirements 그리드는 필요에 맞게 사용자 지정을 할 수 있습니다. 예를 들어 그리드에 표시할 열을 결정할 수 있으며 필터를 사용하여 특정 requirement만 표시할 수 있습니다. [requirement 그리드 사용자 지정에 대한 자세한 내용을 참조하세요.](#configure-the-requirements-grid)

- **B1: Groups**: [group your requirements by column headers](#group-requirements-by-column-headers)로 열(column)을 드래그 앤 드롭 하세요.
- **B2: Column header**: 열 헤더에는 열 캡션(caption)이 표시됩니다. [그리드에 표시할 열](#toggle-and-rearrange-the-columns)을 설정할 수 있으며 [오름차순 및 내림차순으로 열을 정렬](#change-the-sorting-order)할 수 있습니다.
- **B3: Quickfilter**: 빠른 필터(quick filter)를 사용하면 검색어를 기준으로 전체 그리드 컨텐츠를 필터링 할 수 있습니다.
- **B4: Reset grid to preset**: ![](images/result-icon.png){class="intxt-image"}를 프리셋(preset)으로 되돌리기 위해 ![alt text](images/reset-icon.png){class="intxt-image"}를 클릭합니다. ![](images/project-icon.png){class="intxt-image"}**Project**의 requirement 그리드에서는 해당 버튼은 아무 기능도 하지 않습니다.
- **B5: Clear all filters**: 열의 헤더에서 quick 필터와 모든 필터들을 되돌리기 위해 ![alt text](images/reset-filter-icon.png){class="intxt-image"}를 클릭합니다. 만약 필터가 설정되어 있다면 아이콘은 빨간색입니다. 
- **B6: Autosize all columns**: 열의 컨텐츠들에 대해서 열의 너비가 조정됩니다.
- **B7: Columns**: 표시하거나 하지 않은 열을 선택하기 위한 토글(toggle)창을 표시하기 위해 ![alt text](images/columns-icon.png){class="intxt-image"}를 클릭합니다. 여기에서 구성한 보기(view)를 저장할 수 있습니다.

![alt text](images/requirements-grid.png)

##### C: Add button

[프로젝트에 MDM requirements를 추가](#add-requirements-and-test-cases-to-the-project)하기 위해 **Add** 버튼을 클릭합하려면

##### D: Side panel

requirement를 클릭한 다음 ![alt text](images/left-side-two-arrow.png){class="intxt-image"}로 측면 패널(side panel)을 확장하여 requirement에 대한 자세한 정보를 확인합니다. 측면 패널을 다시 축소하려면 ![alt text](images/right-side-two-arrow.png){class="intxt-image"} 클릭합니다.

![alt text](images/side-panel.png)

###### Status
 
선택한 requirement의 현재 상태가 여기에 표시됩니다. 상태는 특정 시점의 실제 값을 나타냅니다. 이 값에는 주석(comment)이나 첨부 파일과 같은 선택적 속성이 함께 표시될 수 있습니다. 이 값은 기존 임계값과 비교되며 결과에 따라 빨간색, 노란색 또는 녹색과 같은 특정 색상으로 표시됩니다. 이 영역에는 다음과 같은 정보가 표시됩니다.

- 현재 값, 주석(comment) 그리고 업로드된 문서들
- 사용자와 최근 상태에 대한 날짜 - 자동으로 문서화됨
- [상태를 수동으로 보고(report)](#manually-report-the-status)하기 위한 버튼

![alt text](images/status-image.png)

###### Details

세부 정보 패널에는 이름, 설명 및 테스트 결과의 식별자와 같은 추가 requirement 속성이 표시됩니다. [Requirements](#mdm-requirements)에서 확인하세요.

![alt text](images/details-image.png)

###### Thresholds

여기에는 requirements 결정에 대한 제한 또는 기준에 대한 자세한 정보가 나와 있습니다.
현재 프로젝트 상태의 경우 임계값의 구성에 따라 평가(assessment)가 계산됩니다.

![alt text](images/threadholds-image.png)

###### Context

이 패널에는 requirement 범위(scope) 및 콘텐츠를 설명하는 데 사용되는 속성과 값이 표시됩니다.
[MDM requirements](#mdm-requirements)을 참조하세요.

![alt text](images/context-image.png)

###### History

requirements의 변경 사항은 기록 패널(history panel)에서 추적할 수 있습니다.
여기에는 다음 정보가 문서화되어 있습니다.

- 변경을 수행한 사람의 이름
- 변경 유형 및 변경 날짜

![alt text](images/history-image.png)

###### Attachments

이 패널에는 MDM requirements에 첨부된 문서가 표시되어 requirement에 대한 일반적인 정보를 제공합니다.

![alt text](images/attachments-image.png)

##### Context menu

개요(overview)에서 requirement을 마우스 오른쪽 버튼으로 클릭하여 상황에 맞는 메뉴에 접근합니다. 컨텍스트(context) 메뉴에는 다음과 같은 옵션이 포함되어 있습니다.

- ![alt text](images/edit-test-case.png){class="intxt-image"} [Edit test case](#edit-a-test-case-to-be-project-specific): 테스트 케이스(test case)를 프로젝트별로 편집할 수 있는 창을 엽니다.
- ![alt text](images/duplicate-test-case.png){class="intxt-image"} **Duplicate test case**: 테스트 케이스(test case)의 복사본을 생성하고 해당 복사본의 설정을 편집할 수 있는 창을 엽니다.
- ![alt text](images/remove-test-case.png){class="intxt-image"} **Remove test case**: 프로젝트에서 테스트 케이스(test case)(모든 requirements와 함께)를 제거합니다.
---

- ![](images/edit-test-case.png){class="intxt-image"} [Edit requirement](#edit-one-requirement-to-be-project-specific): Requirement를 프로젝트별로 편집할 수 있는 창이 열립니다.
- ![alt text](images/duplicate-test-case.png){class="intxt-image"} **Duplicate requirement**: requirement의 복사본을 만들고 해당 복사본의 설정을 편집할 수 있는 창을 엽니다.
- ![alt text](images/remove-test-case.png){class="intxt-image"} **Remove requirement**: 프로젝트에서 requirement를 제거합니다.

![alt text](images/context-image.png)

#### Settings

**Settings** 영역에서 프로젝트 이름, 유형, 설명 및 아이콘을 편집할 수 있습니다. 이 영역은 해당 권한이 있는 사용자만 액세스할 수 있습니다.

![alt text](images/settings.png)

#### Project members

프로젝트 멤버 영역에서는 프로젝트 멤버와 각자의 역할에 대한 개요(overview)를 확인할 수 있습니다. 여기에는 다음 정보가 문서화되어 있습니다.

- 프로젝트 멤버의 이름
- 프로젝트 역할
- 이러한 역할을 지정한 사용자의 이름
- 역할이 할당된 날짜

이 영역은 해당 권한이 있는 사용자만 액세스할 수 있습니다. [새 프로젝트 멤버 추가에 대한 자세한 정보를 확인하세요.](#add-project-members)

![alt text](images/project-members.png)

## Configuration

Configuration 영역은 다음으로 접근할 수 있습니다.

1. 상단 오른쪽에 있는 ![alt text](images/three-horizontal-icon.png){class="intxt-image"}를 클릭합니다.
2. 이 메뉴에서 **Configuration**을 클릭합니다.
3. 그러면 아래와 같이 세로 탐색 모음과 함께 구성 보기가 열립니다.

![alt text](images/configuration.png)

### Master data management (MDM)

MDM은 마스터 데이터 관리(Master Data Management)의 약자입니다. 이는 SCALE.sdm 전체에서 사용되는 속성, 요구 사항 및 테스트 사례를 관리하는 중앙 허브입니다. 마스터 데이터 레코드는 일관되고 정확한 데이터의 단일 소스를 제공하므로 마스터 데이터 레코드를 생성하는 것이 유리합니다.

:::{line-block}
**Example: Attributes**
자동차를 설계하면서 충돌 안전성을 테스트하고 싶다고 가정해 보겠습니다. 특히 자동차가 정면 장애물, 움직이는 측면 장애물 등 다양한 장애물에 충돌할 때 자동차가 어떻게 작동하는지 알고 싶다고 가정해 보겠습니다.

1. 먼저 필요한 모든 속성을 생성합니다. 즉, **Configuration** > **MDM** > **Attributes**으로 이동하여 "Fixed", "MDB", "MPDB", "ODB" 및 "Pole"이라는 값으로 "Barrier"이라는 속성을 생성합니다.
2. 둘째, 각 시나리오에 적합한 속성을 선택합니다. 즉, 정면 충돌 테스트에서는 "Fixed" (barrier)을 선택합니다. 그리고 측면 충격 테스트에는 "MDB" 방벽(barrier)을 선택합니다.

이 예에서 볼 수 있듯이, 데이터는 처음에 MDM에서 생성된 다음 관련 시나리오에서 선택됩니다. 데이터는 단일 소스에서 비롯되므로 데이터가 사용되는 모든 곳에서 일관되고 정확하게 유지됩니다.

**Who creates master data?**
마스터 데이터는 키(key) 사용자 또는 관리자(admin)와 같이 해당 권한이 있는 사람만 만들 수 있습니다. 또한 마스터 데이터(master data)는 관련 시나리오에서 선택하기 전에 먼저 생성되어야 합니다. 즉, 관리자 또는 키 사용자가 먼저 마스터 데이터를 만들어야 SCALE.sdm으로 적극적으로 작업을 시작할 수 있습니다.
:::

#### MDM attributes

- [What are attributes?](#what-are-attributes)
- [View attributes in the overview](#view-attributes-in-the-overview)
- [Add new attributes](#add-new-attributes)
- [Attribute components](#attribute-components)
    - [Add new attribute components](#add-new-attribute-components)
    - [Apply components to attributes](#apply-components-to-attributes)
    - [Use attributes with components](#use-attributes-with-components)
- [Attribute value lists](#attribute-value-lists)
    - [Add new attribute value lists](#add-new-attribute-value-lists)
    - [Apply value lists to attributes](#apply-value-lists-to-attributes)
    - [Use attributes with value lists](#use-attributes-with-value-lists)

##### What are attributes?

Attributes은 ![](images/project-icon.png){class="intxt-image"} **프로젝트** 및 ![](images/result-icon.png){class="intxt-image"} **Result** 내에서 다양한 용도로 사용됩니다. 

- **Attributes provide context**. 즉, 프로젝트, 테스트 케이스 또는 requirement을 추가로 설명합니다. 이러한 컨텍스트 속성의 몇 가지 예는 다음과 같습니다.

    - 프로젝트의 대상 시장(예: 북미, 유럽).
    - 사용 중인 충돌 테스트 더미의 유형(예: ES-2, HIII-50%(H3), HIII-5%(HF), SID IIs(S2))
    - 사용 중인 배리어(barrier) 유형(예: Fixed, MDB, MPDB, ODB, Pole)

- **Attributes identify test results**. 즉, requirement를 평가하는 기준을 제공합니다. 이러한 속성의 몇 가지 예는 다음과 같습니다.

    - Head acceleration(G)
    - Chest deflection(mm)
    - Femur force(kN)

##### View attributes in the overview

**Configuration** > **MDM** > **Attributes**으로 이동하여 사용 가능한 attributes에 대한 개요를 확인합니다. 개요의 데이터를 오름차순 또는 내림차순으로 필터링하고 정렬할 수 있습니다. 이렇게 하면 현재 작업과 관련된 데이터만 표시할 수 있습니다.

![alt text](images/view-attributes-in-the-overview.png)

##### Add new attributes

- **Configuration** > **MDM** > **Attributes**으로 이동합니다.
- 오른쪽 상단 모서리에서 **New**를 클릭합니다. 새 창이 열립니다.
- 필요에 따라 설정을 구성합니다. 각 설정에 대한 설명은 아래 표에 나와 있습니다.
- ![alt text](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다. 속성이 개요에 나타납니다.

![alt text](images/add-new-attributes.png)

<!-- | Setting | Explanation |
| ---- | ---- |
| Identifier | SCALE.sdm에 속성을 고유하게 식별하는 이름을 입력합니다. 즉, 다른 속성에 이미 사용되고 있지 않은 이름을 입력합니다. **참고**: 식별자(identifier)가 반드시 특정 명명 패턴을 따를 필요는 없습니다. 그러나 ISO-MME와 같은 명명 패턴은 특히 대규모 데이터베이스로 작업하는 경우 식별자를 추적하는 데 도움이 될 수 있으므로 실무에서 자주 사용됩니다. **참고**: 대문자와 소문자 사용에 유의하세요. "Market", "market", "MARKET"이라는 단어는 모두 고유한 것으로 간주됩니다. |
| -->

:::{list-table}
:widths: 15 100
:header-rows: 1

*   - Setting
    - Explanation    
*   - Identifier
(required)
    - SCALE.sdm에 속성을 고유하게 식별하는 이름을 입력합니다. 즉, 다른 속성에 이미 사용되고 있지 않은 이름을 입력합니다. 
    참고: 식별자가 반드시 특정 명명 패턴을 따를 필요는 없습니다. 그러나 ISO-MME와 같은 명명 패턴은 특히 대규모 데이터베이스로 작업하는 경우 식별자를 추적하는 데 도움이 될 수 있으므로 실무에서 자주 사용됩니다.
    참고: 대문자와 소문자 사용에 유의하세요. "Market", "market", "MARKET" 이라는 단어는 모두 고유한 것으로 간주됩니다.
*   - Name
(required)
    - 사람이 읽을 수 있는 속성 이름을 입력합니다.
*   - Component
    - 속성이 속한 컴포넌트를 선택합니다. 사용 사례: 컴포넌트는 특정 카테고리 아래에 속성을 그룹화하는 방법입니다. [컴포넌트에 대한 자세한 정보를 확인하세요.](#attribute-components)
*   - Obsolete
    - 속성이 더 이상 사용되지 않는 경우 이 옵션을 선택합니다![](images/check-box-icon.png){class="intxt-image"}. 사용 사례: 활발하게 사용되지 않는 속성을 삭제하는 대신 사용되지 않는 것으로 표시할 수 있습니다.
*   - Usable as association attribute
    - 속성(attribute)을 연결/컨텍스트(association/context) 속성으로 사용해야 하는 경우(예: 요구 사항) 이 옵션을 선택합니다![](images/check-box-icon.png){class="intxt-image"}.
*   - Description
    - 다른 사용자가 볼 수 있도록 속성(attribute)에 대한 설명을 입력합니다.
*   - Comment
    - 설명에 필요하지 않은 속성에 대한 설명을 입력합니다.
*   - Attribute type
    - 속성(attribute)을 결과 또는 설명으로 사용할지 여부에 대한 옵션입니다.
*   - Data type
(required)
    - 속성(attribute)이 나타내는 데이터 유형은 무엇인가요? 드롭다운 목록에서 적절한 유형을 선택합니다.
    **Boolean** = 속성 값이 true인지 false인지 나타냅니다.
    **Datetime** = 속성 값이 날짜(date)와 시간(time) 입니다. 예를 들어 테스트가 수행되었던 때의 날짜와 시간입니다.
    **Number** = 속성 값이 숫자입니다. 예로 차량 스피드가 있습니다. **Display units**에서 단위를 선택합니다.
    **Text** = 속성 값은 미리 정의된 여러 옵션 중 하나입니다. 예를 들어 "CNCAP", "Euro NCAP", "FMVSS" 또는 "USNCAP" 지시어가 있습니다. **Value list**에서 미리 정의된 옵션 집합을 선택합니다. [속성 값 목록에 대한 자세한 내용을 참조하세요.](#attribute-value-lists)
:::

##### Attribute components

컴포넌트(Components)는 특정 카테고리로 속성(attributes)을 그룹화하는 방법입니다. 예를 들어

- 'battery' 또는 'fuel pump'와 같은 특정 자동차 부품에 대한 그룹을 만들 수 있습니다. 그런 다음 값을 측정할 때 이러한 값은 해당 구성 요소에 따라 함께 그룹화됩니다.
- 함께 평가해야 하는 속성을 그룹화할 수도 있습니다. 예를 들어 'doors unlocked during crash'이라는 컴포넌트를 만들 수 있습니다. 그런 다음 값이 측정될 때 이 값은 문이 잠겼는지 또는 잠금이 해제되었는지 여부를 지정합니다.

###### Add new attribute components

1. **Configuration** > **MDM** > **Attribute components**로 이동합니다.
2. 상단 오른쪽 모서리에서 **New**를 클릭합니다.
3. 구성 요소(component)의 이름을 입력합니다. 원하는 경우 설명을 입력하거나 구성 요소를 더 이상 사용되지 않는 것으로 표시합니다.
4. ![](images/save-icon.png){class="intxt-image"} 버튼을 클릭하여 설정을 저장합니다. 

![alt text](images/add-new-attribute-components.png)

###### Apply components to attributes

1. **Configuration** > **MDM** > **Attributes**로 이동합니다.
2. 설정을 열기 위해서 존재하는 속성(attribute)을 클릭하든지 **New**를 클릭하여 새 속성을 만듭니다.
3. 구성 요소(compoenent)에서 속성이 속한 구성 요소(compoenent)를 선택합니다.
4. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다.

###### Use attributes with components

이제 속성(attributes)이 표시되면 해당 구성 요소 이름 아래에 속성이 함께 그룹화됩니다. 예를 들어 ![](images/result-icon.png){class="intxt-image"}**Result**에서는 테스트 세부 정보 페이지에서 속성이 구성 요소별로 그룹화됩니다.

![alt text](images/example-for-grouping-attributes-by-component.png)

##### Attribute value lists

미리 정의된 여러 옵션의 목록을 만들 수 있습니다. 예를 들어 "CNCAP", "Euro NCAP", "FMVSS" 또는 "USNCAP" 옵션이 포함된 "Directive"라는 목록을 만들 수 있습니다. 이는 속성(attribute) 값 목록을 생성하여 수행됩니다.

###### Add new attribute value lists

1. **Configuration** > **MDM** > **Attribute value lists** 값 목록으로 이동합니다.
2. 오른쪽 하단을 ![](images/black-plus.png){class="intxt-image"} 클릭합니다. 새 창이 열립니다.
3. 목록의 이름을 입력합니다. 예: "Directive".
4. 오른쪽 아래 모서리에 있는 **New value**을 클릭합니다. 팝업 창이 열립니다.
5. 값의 이름과 레이블을 입력합니다. 예: "CNCAP". 레이블은 값 목록 내에서 적용하여 속성(attribute) 값으로 볼 수 있는 값입니다.
6. **Save**을 클릭합니다. 값이 목록에 추가됩니다. 같은 방법으로 다른 값을 추가합니다. 예를 들어 "Euro NCAP", "FMVSS" 및 "USNCAP" 값을 추가합니다.
7. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 모든 값과 함께 목록을 저장합니다.

![alt text](images/add-new-attribute-value-lists.png)

###### Apply value lists to attributes

속성(Attribute) 값 목록은 데이터 유형이 텍스트인 속성에만 적용할 수 있습니다.

1. **Configuration** > **MDM** > **Attributes**으로 이동합니다.
2. **New**를 클릭하여 새 속성(attribute)을 만들거나 기존 속성을 클릭하여 해당 설정을 엽니다.
3. **Data type**을 **Text**로 옵션을 설정합니다.
4. **Value list**에서 속성(attribute) 값 목록을 선택합니다.
5. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다.

###### Use attributes with value lists

이제 속성(attribute)과 해당 값을 사용할 준비가 되었습니다. 값은 목록에 표시됩니다. 예를 들어 프로젝트에서 속성(attribute)과 해당 값을 사용하여 프로젝트에 대한 추가 컨텍스트(context)를 제공할 수 있습니다.

![alt text](images/example-for-using-attributes-with-value-lists.png)

#### MDM requirements

- [Overview](#overview-1)
- [View details about a requirement](#view-details-about-a-requirement)
    - [Details](#details-1)
    - [Thresholds](#thresholds-1)
    - [Context](#context-1)
    - [Attachments](#attachments-1)
    - [History](#history-1)
- [Add new requirements](#add-new-requirements)
    - [Assessment](#assessment)
    - [Context](#context-1)
    - [Attachments](#attachments-1)
- [Options in the context menu](#options-in-the-context-menu)
- [Edit multiple requirements at once](#edit-multiple-requriements-at-ones)
    - [Edit the names](#edit-the-names-1)
    - [Edit the descriptions](#edit-the-descriptions-1)
    - [Edit the test result identifiers](#edit-the-test-result-identifiers)
    - [Edit the assessment thresholds](#edit-the-assessment-thresholds-1)

---

Requirements은 기술 프로젝트 목표와 관련하여 테스트 결과를 평가하기 위해 사용자가 정의합니다. 따라서 각 requirement은 단일 스칼라(scalar) 테스트 결과의 평가와 동일하지만, 평가(evaluation)는 사용자가 색상 등급 간격을 기준으로 점진적으로 정의할 수 있습니다.

:::{admonition} MDM requirements vs. project requirements
:class: tip
- **MDM requirements**: **Configuration** > **MDM** > **Requirements** 아래의 requirements을 MDM requirements이라고 합니다. requirement 템플릿 또는 SCALE.sdm 애플리케이션에 대한 전역 requirement 데이터베이스라고 생각할 수 있습니다.

- **Project requirements**: 특정 프로젝트 내의 requirements을 project requirements이라고 합니다. project requirements는 MDM requirements에서 파생됩니다. 이 과정에서 원래 requirement의 속성, 임계값 등이 프로젝트별 requirement으로 복사되며 필요한 경우 추가로 변경할 수 있습니다. 프로젝트에는 동일한 MDM requirements에서 파생된 여러 project requirements이 있을 수 있습니다.
:::

##### Overview

**Configuration** > **MDM** > **Requirements**으로 이동하여 사용 가능한 requirements의 개요(overview)를 확인합니다. 개요의 데이터는 오름차순 또는 내림차순으로 필터링, 그룹화 및 정렬할 수 있습니다. 열(column)은 켜고 끌 수 있습니다. 이를 통해 현재 작업과 관련된 데이터만 표시할 수 있습니다.

![alt text](images/overview-of-mdm-requirements.png)

:::{admonition} Internal vs. external requirements
:class: tip
- **Internal**: Internal requirements는 수동으로 개요(overview)에 추가합니다.
- **External**: External test case들은 개요(overview)로 가져옵니다.

두 가지 유형의 requirements 모두 추가로 편집하거나 삭제할 수 있습니다.
:::

##### View details about a requirement

1. **Configuration** > **MDM** > **Requirements**로 이동합니다.
2. Overview에서 requirement를 클릭합니다.
3. 상단 오른쪽 모서리의 ![](images/left-side-two-arrow.png)를 클릭합니다. 추가로 사이드 패널이 표시되며 다음 항목들이 포함됩니다.

    - [Detail](#details-1)
    - [Thresholds](#thresholds-1)
    - [Context](#context-1)
    - [Attachments](#attachments-1)
    - [History](#history-1)

![alt text](images/overview-with-expanded-side-panel.png)

###### Details

여기에서 requirement을 정의하는 일반 속성(properties)을 볼 수 있습니다.

- **Name** - 필수 - 서로 다른 requirements을 구분하기 위한 필수 중요 이름 매개변수입니다.
- **Description** - 선택 사항 - requirement에 대한 추가 텍스트 설명입니다.
- **Test result identifier** - 필수 - requirement이 평가되는 기준이 되는 속성(attribute)입니다.

###### Thresholds

requirement 임계값(thresholds)(주어진 한도 또는 기준)은 가중치 간격에 따라 점진적으로 정의됩니다. 각 평가 수준은 색상으로 표시되어 사용자에게 동의 여부를 강조합니다.

requirement에 대한 테스트 속성 값의 동의 여부는 <span style="color:green">녹색</span>, <span style="color:yellow">노란색</span>, <span style="color:orange">주황색</span>, <span style="color:brown">갈색</span> 및 <span style="color:red">빨강색</span>으로 강조 표시된 범위로 가중치를 부여할 수 있습니다. 가중치가 없는 <span style="color:gray">회색</span> 평가도 있습니다.

:::{admonition} Threshold ranks can be customized
:class: tip
고급 권한(advanced permmision)이 있는 사용자는 MDM 임계값(thresholds) 등급을 사용자 지정할 수 있습니다. 즉, 고급 권한이 있는 사용자는 다음을 결정할 수 있다는 것을 의미합니다.

- 임계값에 어떤 색상과 이름을 사용할지
- 얼마나 많은 임계값이 필요한지
- 임계값의 순위를 매길 순서(가장 높은 것부터 가장 낮은 것까지)
- 사용자는 **MDM** > **MDM threshold rank** 권한이 있고 사용자 계정이 **Staff**으로 표시된 경우에만 임계값(thresholds) 순위를 사용자 지정할 수 있습니다. 이러한 권한이 설정되어 있으면 사용자는 **Admin area**에서 임계값 순위를 사용자 지정할 수 있습니다. [권한에 대한 자세한 내용을 참조하세요.](./scale-result.md/#permissions)
:::

###### Context

**Context Attributes**을 사용하여 사용자는 특정 지시어(directive), 충돌 실험 구성 또는 더미(dummy) 유형과 관련된 요구 사항의 기술적 적용 컨텍스트를 지정할 수 있습니다. 사용자는 MDM Attribute 값 목록 목록으로 컨텍스트를 정의할 수 있으며, 각 속성 키에 대해 여러 목록 값을 할당할 수 있습니다. 컨텍스트 그룹을 사용하여 **Context Groups**을 그룹화할 수 있습니다.

**Context Attributes** 목록을 기반으로 테스트와 관련 테스트 결과를 자동으로 매칭하여 project requirements에 대한 테스트 결과를 안내에 따라 보고할 수 있습니다.

###### Attachments

각 requirement은 실험 지침(experimental guidelines), 기술 스케치(technical sketches) 또는 일반 문서 등 증빙 파일을 첨부하여 지정할 수 있습니다.

###### History

Requirement 변경은 기록 패널에서 사용자를 추적되고 추적할 수 있습니다. 누가 몇 시에 무엇을 변경했는지에 대한 요약이 시간순으로 정렬된 목록으로 사용자에게 표시됩니다.

##### Add new requirements

1. **Configuration** > **MDM** > **Requirements**로 이동합니다.
2. ![](images/plus-only-icon.png){class="intxt-image"} **New**를 클릭합니다.
3. 필요에 따라 설정을 구성합니다. 기본 설정과 **Assessment**, **Context** 및 **Attachments** 섹션에 대한 설명은 아래에 자세히 나와 있습니다.
4. ![](images/save-icon.png){class="intxt-image"}를 클릭하고 설정을 저장합니다. requirement는 개요에 표시됩니다.

![alt text](images/adding-a-new-requirement.png)

:::{list-table}
:widths: 15 100
:header-rows: 1

*   - Setting
    - Explanation    
*   - Name (required)
    - requirement의 이름을 입력합니다.
*   - Description
    - requirement의 설명을 입력합니다.
*   - MDM attribute (required)
    - 테스트 결과 식별자(예: MDM 속성)를 입력합니다. 이 필드에는 자동 완성 기능이 있어 입력을 시작할 때 나머지 단어를 예측합니다. 참고: 검사 결과 식별자가 단위가 있는 숫자인 경우(예: chest deflection(mm)), 여기에도 단위가 표시됩니다.
*   - Attribute key
    - MDM 속성에 와일드카드(예: 자리 표시자(placeholder) ?)가 포함되어 있는 경우 이 필드를 사용하여 requirement가 적용되는 정확한 MDM 속성을 지정할 수 있습니다. 예: 더미(dummy)에 대한 속성을 만들고 와일드카드를 사용하여 해당 속성이 더미(dummy) 1~6에 적용되도록 했다고 가정해 보겠습니다. 이제 requirement가 더미(dummy) 2에만 적용되도록 하려면 속성 키(attribute key)를 사용하여 이를 지정하면 됩니다.
*   - Display unit
    - 이 필드는 검사 결과 식별자가 단위가 있는 숫자인 경우에만 표시됩니다(예: chest deflection(mm)).
:::

###### Accessment

임계값을 추가하려면 ![](images/black-plus.png){class="intxt-image"}를 클릭합니다. 왼쪽에서 임계값(thresholds)의 색상을 선택합니다. 오른쪽에서 임계값(thresholds)의 상한과 하한을 정의합니다. 평가 임계값(assessment thresholds) 간에는 종속성이 없습니다. 범위 열에 +-inf 및 --inf를 입력하여 무한대를 상한 및 하한으로 설정할 수 있습니다. '보다 작음'(**<**) 및 '보다 같음'(![alt text](images/less-than-or-equal.png)) 기호를 클릭하여 이 두 모드 사이를 전환할 수 있습니다.

![alt text](images/assessment.png)

###### Context

먼저 **Add Context group**을 클릭합니다. 컨텍스트 그룹(context group)은 유사한 컨텍스트 속성(context attributes)의 지정되지 않은 집합으로 생각할 수 있습니다. 이제 왼쪽에 속성(attribute)을 입력하고 오른쪽에 하나 또는 여러 개의 속성 값(attribute values)을 추가할 수 있습니다. 참고: 속성 목록에는 연결 속성만 포함되어 있습니다. 컨텍스트 그룹에 추가 속성을 추가하려면 ![](images/black-plus.png){class="intxt-image"}를 클릭합니다.

![alt text](images/context.png)

###### Attachments

![](images/black-plus.png){class="intxt-image"}를 클릭하고 [](#attachments-1)를 선택합니다.

![alt text](images/attachments.png)

##### Options in the context menu

개요(overview)에서 requirement를 마우스 오른쪽 버튼으로 클릭하여 상황에 맞는 메뉴에 액세스합니다. 상황에 맞는 메뉴에는 다음과 같은 옵션이 포함되어 있습니다.

- **Edit**: 편집 화면을 엽니다. 이 화면에는 새 requirement를 추가할 때 사용할 수 있는 것과 동일한 옵션이 포함되어 있습니다.
- **Copy**: 복사한 requirement를 복제하고 이름에 (Copy)가 추가된 편집 모드에서 엽니다.
- **Toggle active**: 상태를 활성에서 비활성으로 또는 그 반대로 전환합니다.
- **Delete**: requirement를 삭제합니다.

![alt text](images/Using-the-context-menu.png)

##### Edit multiple requriements at ones

1. **Configuration** > **MDM** > **requirements**으로 이동합니다.
2. 개요(overview)에서 여러 requirements를 선택한 다음(Ctrl. + 클릭) 마우스 오른쪽 버튼을 클릭합니다. 컨텍스트 메뉴가 열립니다. 컨텍스트 메뉴의 옵션은 선택한 모든 requirements와 관련이 있습니다.
3. **Edit**를 클릭합니다. 새 창이 열립니다. 여기에서 선택한 모든 requirements의 이름, 설명, 테스트 결과 식별자 및 평가 임계값(assessment thresholds)을 동시에 편집할 수 있습니다.

###### Edit the names

1. 체크 박스 ![](images/check-box-icon.png){class="intxt-image"}를 클릭합니다.
2. **Change to apply** 드롭다운 목록에서 옵션을 선택합니다.
    - **Replace**: requirement 이름 내에서 특정 단어 하나를 변경합니다.
    - **Replace all**: 전체 requirement 이름을 변경합니다.
    - **Add to beginning**: requirement 이름의 시작 부분에 특정 텍스트를 추가합니다.
    - **Add to end**: requirement 이름 끝에 특정 텍스트를 추가합니다.
3. 텍스트 필드에 텍스트를 입력합니다.
4. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다.

![alt text](images/example-correct-a-typo-in-both-requirement-names.png)

###### Edit the descriptions

1. **Description** 필드 옆의 ![](images/check-box-icon.png){class="intxt-image"}를 체크합니다.
2. **Description** 필드에 텍스트를 입력합니다.
3. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다.

![alt text](images/example-update-the-descriptions-of-both-requirements.png)

###### Edit the test result identifiers

1. **Test result identifier** 필드 옆의 체크박스 ![](images/check-box-icon.png){class="intxt-image"}를 선택합니다.
2. 테스트 결과 식별자(test result identifier)를 입력합니다. 이 필드에는 자동 완성 기능이 있어 입력을 시작할 때 나머지 단어를 예측합니다.
3. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다. 테스트 결과 식별자(test result identifier)가 변경됩니다.

###### Edit the assessment thresholds

1. **Apply Changes to all Assessments** 영역을 펼칩니다.
2. 체크박스 ![](images/check-box-icon.png){class="intxt-image"}을 선택합니다.
3. 필요에 따라 평가 임계값(assessment thresholds)을 수정합니다. 절차는 새 requirement에 대한 평가 임계값을 저장할 때와 동일합니다.
4. ![](images/save-icon.png){class="intxt-image"}을 클릭하여 설정을 저장합니다.

#### MDM test cases

- [Overview](#overview-2)
- [View details about a test case](#view-details-about-a-test-case)
- [Add new test cases](#add-new-test-cases)
- [Options in the context menu](#options-in-the-context-menu-1)

---

일반적으로 requirement은 혼자 오지 않습니다. 따라서 requirements를 테스트 케이스로 그룹화할 수 있습니다. 테스트 케이스(test case)에는 하나 이상의 requirements가 있으며 단일 requirement의 컨텍스트와 유사한 컨텍스트를 정의합니다. 테스트 케이스 컨텍스트는 테스트 케이스가 특정 테스트에 적용 가능한지 여부를 지정합니다.

:::{admonition} MDM test cases vs. project test cases
:class: tip
- **MDM test cases:** ![](images/three-horizontal-icon.png) > **Configuration** > **MDM** > **Test cases**에 있는 테스트 케이스를 MDM test case라고 합니다. 템플릿 또는 SCALE.sdm 애플리케이션을 위한 글로벌 데이터베이스라고 생각할 수 있습니다.

- **Project test cases:** 특정 프로젝트 내의 테스트 케이스를 프로젝트 테스트 케이스라고 합니다. 프로젝트 테스트 케이스는 MDM 테스트 케이스에서 파생됩니다. 이 과정에서 원래 테스트 케이스의 컨텍스트, 요구 사항 등이 프로젝트별 테스트 케이스에 복사되며 필요한 경우 추가로 변경할 수 있습니다. 프로젝트에는 동일한 MDM test case에서 파생된 여러 프로젝트 테스트 케이스가 있을 수 있습니다.
:::

##### Overview

![](images/three-horizontal-icon.png){class="intxt-image"} > **Configuration** > **MDM** > **Test cases**로 이동하여 테스트 사례의 개요를 확인하세요. 개요의 데이터는 오름차순 또는 내림차순으로 필터링, 그룹화 및 정렬할 수 있습니다. 열은 켜고 끌 수 있습니다. 이를 통해 현재 작업과 관련된 데이터만 표시할 수 있습니다.

![alt text](images/overview-of-mdm-test-cases.png)

##### View details about a test case

1. ![](images/three-horizontal-icon.png){class="intxt-image"} > **Configuration** > **MDM** > **Test cases**로 이동합니다.
2. 개요에서 test case를 클릭합니다.
3. 오른쪽 상단 모서리의 ![](images/double-left-arrow.png){class="intxt-image"}를 클릭합니다. 사이드 패널이 확장됩니다. 여기에는 테스트 케이스 및 해당 컨텍스트에 대한 세부 정보가 포함되어 있습니다.

##### Add new test cases

1. ![](images/three-horizontal-icon.png){class="intxt-image"} **Configuration** > **MDM** > **Test cases**로 이동합니다.
2. 오른쪽 상단 모서리에서 ![](images/plus-only-icon.png) **New**를 클릭합니다. 새 창이 열립니다.
3. 필요에 따라 설정을 구성합니다. 설정에 대한 설명은 아래 표에 나와 있습니다.
4. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다. overview에 테스트 케이스(test case)가 나타납니다. 

![alt text](images/adding-a-new-test-case.png)

:::{list-table}
:widths: 15 100
:header-rows: 1

*   - Setting
    - Explanation    
*   - **Name** (required)
    - test case의 이름을 입력합니다.
*   - **Description**
    - test case의 설명을 입력합니다.
*   - **Comment**
    - test case에 대한 코멘트를 입력합니다.
*   - **Discipline**
    - test case에 대한 하나 이상의 분야를 선택합니다.
*   - **State** (required)
    - test case가 활성 상태인지 비활성 상태인지 지정합니다.
*   - **Requirements** (required)
    - test case에 포함되어야 하는 모든 요구 사항(requirements)를 체크하세요 ![](images/check-box-icon.png){class="intxt-image"}. 이 그리드의 요구 사항을 필터링, 그룹화 및 정렬하여 현재 작업과 관련된 데이터를 찾을 수 있습니다.
참고: 요구 사항을 그룹화한 경우 전체 그룹을 선택할 수 있습니다(위 이미지 참조). 그러면 해당 그룹의 모든 요구 사항이 선택됩니다. 전체 그룹을 선택하면 각 요구 사항을 개별적으로 확인할 필요가 없으므로 시간을 절약할 수 있습니다.
*   - **Context**
    - 먼저 **Add Context group**을 클릭합니다. 컨텍스트 그룹(context group)은 주제적으로 유사한 컨텍스트 속성의 지정되지 않은 집합으로 생각할 수 있습니다. 이제 왼쪽에 속성을 입력하고 오른쪽에 하나 또는 여러 개의 속성 값을 추가할 수 있습니다. 참고: 속성 목록에는 [연결 속성(association attributes)](#add-new-attributes)만 포함되어 있습니다. 컨텍스트 그룹에 추가 속성을 추가하려면 ![](images/black-plus.png){class="intxt-image"} 클릭합니다.
:::

##### Options in the context menu

개요(overview)에서 테스트 케이스(test case)를 마우스 오른쪽 버튼으로 클릭하여 컨텍스트 메뉴에 액세스합니다. 컨텍스트 메뉴에는 다음과 같은 옵션이 있습니다.

- **Copy**: 복사한 테스트 케이스를 복제하고 테스트 이름에 (_copy_)를 추가하여 편집 모드에서 엽니다. 이 옵션은 외부(external) 및 내부(internal) 테스트 케이스 모두에 사용할 수 있습니다. 참고: 외부 테스트 케이스를 복사하는 경우 복제본은 내부 테스트 케이스가 됩니다.
- **Edit**: 편집 화면을 엽니다. 이 옵션은 내부 테스트 케이스에만 사용할 수 있습니다.
- **Remove**: 테스트 케이스를 삭제합니다. 이 옵션은 내부 테스트 케이스에만 사용할 수 있으며 프로젝트에서 사용되지 않는 테스트 케이스에 대해서만 사용할 수 있습니다.
- **Toggle active**: 상태를 활성에서 비활성으로 또는 그 반대로 전환합니다. 이 옵션은 내부 테스트 케이스에만 사용할 수 있습니다.

![alt text](images/using-the-context-menu-mdm-test-case.png)

:::{admonition} Internal vs. external test cases
:class: tip
- **Internal**: 내부 테스트 케이스들은 수동으로 개요에 추가됩니다. 추가로 편집하거나 삭제 할 수 있습니다.
- **External**: 외부 테스트 케이스들은 개요에서 가져올 수 있습니다. 읽기 전용이므로 편집하거나 삭제할 수 없습니다.
:::

### Presets

Presets는 도메인별 모양과 도메인별 정보를 구성하는 방법입니다. 이는 ![](images/result-icon.png){class="intxt-image"} **Result**의 필수적인 부분입니다. Preset은 XML로 정의되며 소위 "preset bricks"라고 하는 추가 XML 하위 모듈을 참조할 수 있습니다.

프리셋으로 구성된 주요 영역은 다음과 같습니다:

- 기본 그리드의 열(속성, 서식, 데이터 변환)
- 미리 정의된 필터(시나리오 트리)

이 섹션은 여러 부분으로 나뉩니다.

1. [Layout management](#layout-management)
2. [Preset guideline](#preset-guideline)
3. [Tag attributes]()
4. [Conditions]()

#### Layout management

- [Component: Grid](#component-grid)
- [Grid side bar](#grid-side-bar)
    - [Tab: Columns](#tab-columns)
    - [Tab: Tables](#tab-tables)
    - [Tab: Views](#tab-views)
        - [Save your configuration as a view](#save-your-configuration-as-a-view-1)
        - [Switch between views](#switch-between-views)
        - [Share views with other users](#share-views-with-other-users-1)
        - [Additional options](#additional-options)
- [Component: Scenario](#component-scenario)

이 페이지에서는 사전 설정의 영향을 받는 ![](images/result-icon.png){class="intxt-image"}**Result**의 레이아웃 구성 요소에 대해 설명합니다.

##### Component: Grid

테스트의 표 형식 데이터 표현. 각 줄은 하나의 시험에 해당합니다. 시험의 속성은 그리드 열에 표시됩니다. 사전 설정 구성에 따라 일부 열 헤더는 하위 열을 더 집계할 수 있습니다. 열을 확장하려면 **>**를 클릭합니다. 열을 다시 축소하려면 **<**를 클릭합니다.

![alt text](images/grid.png)

##### Grid side bar

일부 사전 설정에는 그리드에 편리하게 표시할 수 있는 것보다 많은 열이 있을 수 있습니다. 사이드 바(![alt text](images/side-bar-icon.png){class="intxt-image"})를 사용하여 표시할 열과 열이 표시되는 순서를 지정할 수 있습니다. 사이드 바는 아래에 설명된 세 개의 탭으로 구성되어 있습니다.

![alt text](images/side-bar-of-the-grid.png)

###### Tab: Columns

여기에서 표시할 열과 표시 순서를 지정할 수 있습니다.

1. 그리드의 맨 오른쪽의 ![](images/side-bar-icon.png){class="intxt-image"}를 클릭합니다. 사이드 바가 확장됩니다.
2. 표시할 열(![](images/check-box-icon.png){class="intxt-image"})을 선택합니다.
3. 선택 사항: 기호 ![alt text](images/six-dot-icon.png) 위로 마우스 커서를 이동합니다. 커서 모양이 (![](images/hand-icon.png){class="intxt-image"}) 모양으로 바뀝니다. 열을 드래그하여 그리드에서 열의 순서를 변경합니다.

###### Tab: Tables

여기에서 preset에 정의된 모든 테이블 목록을 볼 수 있습니다. [preset에 표를 추가하는 방법에 대한 자세한 내용을 참조하세요]().

###### Tab: Views

여기에서 이미 생성된 모든 보기 목록을 볼 수 있으며 새 뷰(view)를 저장할 수 있습니다. 이 기능은 그리드를 구성한 후 나중에 다시 액세스할 수 있도록 구성을 저장하려는 경우에 유용합니다. 예: 서로 다른 두 개의 뷰를 만들 수 있습니다. 각 뷰에는 특정 작업에 필요한 열만 포함됩니다. 작업을 수행할 때 적절한 뷰를 선택하기만 하면 됩니다.

:::{admonition} What does the view define?
:class: tip
뷰(view)는 레이아웃의 다음 측면을 제어합니다:

- 표시되는 열
- 열이 표시되는 순서
- 열을 그룹화할지 여부.
- 필터 적용 여부.
- 열 내용을 오름차순 또는 내림차순으로 표시할지 여부.

참고: 뷰는 열의 크기나 크기를 제어하지 않습니다.
:::

###### Save your configuration as a view

1. 그리드의 맨 오른쪽의 ![](images/side-bar-icon.png){class="intxt-image"}를 클릭합니다. 사이드 바가 확장됩니다.
2. ![alt text](images/setting-icon.png) **Views**를 클릭합니다. 여기에 모든 기존 views 목록이 표시됩니다.
3. ![](images/plus-only-icon.png) **New View**를 클릭합니다.
4. View의 이름을 입력하고 **Save**를 클릭합니다. View가 목록에 추가됩니다.

###### Switch between views

1. 그리드의 맨 오른쪽의 ![](images/side-bar-icon.png){class="intxt-image"}를 클릭합니다. 사이드 바가 확장됩니다.
2. ![](images/setting-icon.png) **Views**를 클릭합니다. 여기에 모든 기존 views 목록이 표시됩니다.
3. View의 이름을 클릭합니다.

###### Share views with other users

다른 사용자와 view를 공유할 수 있습니다. 예를 들어 관리자는 여러 개의 서로 다른 view를 만들 수 있습니다. 각 view에는 특정 작업을 수행하는 데 도움이 되는 열과 필터가 포함되어 있습니다. 그런 다음 관리자는 이러한 view를 해당 작업을 담당하는 동료들과 공유할 수 있습니다.

1. 그리드의 맨 오른쪽의 ![](images/side-bar-icon.png){class="intxt-image"} 클릭합니다. 사이드 바가 확장됩니다.
2. ![](images/setting-icon.png){class="intxt-image"}**Views**를 클릭합니다. 여기에 모든 기존 view 목록이 표시됩니다.
3. view에 대한 추가 옵션을 보려면 ![alt text](images/vertical-three-dot-icon.png){class="intxt-image"} 클릭합니다.
4. ![alt text](images/share-icon.png){class="intxt-image"} **Share**를 클릭합니다. 팝업 창이 열립니다.
5. 드롭다운 목록에서 분야를 선택합니다.
6. ![](images/white-check-icon.png){class="intxt-image"} **Confirm**을 클릭합니다. view가 해당 분야의 모든 사용자와 공유됩니다.

:::{admonition} How do I know which disciplines a user belongs to?
:class: tip
![](images/three-horizontal-icon.png) > **Configuration** > **User management** > **Users**로 이동하여 사용자 계정을 엽니다. **General information** 섹션에서 **Disciplines** 드롭다운 목록을 클릭합니다. 여기에서 사용자가 속한 분야를 확인할 수 있습니다.
:::

###### Additional options

기존 view를 수정한 후 ![](images/vertical-three-dot.png){class="intxt-image"}를 클릭하여 다음 옵션에 액세스합니다:

- ![](images/save-icon.png){class="intxt-image"} **Save**
- ![](images/save-icon.png){class="intxt-image"} **Save as new**
- ![](images/pencil-icon.png){class="intxt-image"} **Rename**
- ![](images/remove-icon.png){class="intxt-image"} **Delete**
- ![](images/home-icon.png){class="intxt-image"} **Set global Default:** 아직 사용자 지정 view를 구성하지 않은 경우 기본 view가 사용됩니다. 글로벌 관리자(global admin)만 기본 view를 만들거나 수정할 수 있습니다. 일반 사용자는 이 view를 편집할 수 없습니다.
- ![](images/share-icon.png){class="intxt-image"} **Share:** 다른 사용자와 view를 공유합니다. [추가 정보](#share-views-with-other-users-1).

변경 사항을 취소하고 view를 원래 구성으로 되돌리려면 ![alt text](images/discard-icon.png){class="intxt-image"} 클릭합니다.

##### Component: Scenario

시나리오(Scenarios)는 그리드에 표시되는 테스트의 범위를 좁힐 수 있는 방법입니다. 예를 들어 특정 충돌 시나리오와 관련된 테스트(예: 차량 속도, 지시 또는 장애물 겹침(barrier overlap))만 표시할 수 있습니다.

- 표시되는 시나리오는 preset에 정의된 시나리오에 따라 다릅니다. [preset에 시나리오를 추가하는 방법에 대한 자세한 내용을 참조하세요]().
- [시나리오를 사용하여 그리드에 테스트를 표시하는 방법에 대한 자세한 정보]().

![alt text](images/scenarios.png)

#### Preset guideline

- [Preset components]()
- [Preset bricks]()
- [Creating a new preset brick]()
- [Adding a preset brick to a preset]()
- [Adding attributes to a preset]()
- [Adding nested attributes]()
- [Adding tables to a preset]()
- [Adding scenarios to a preset]()
    - [Adding conditions to scenario nodes]()
- [Adding column functions]()

---

이 가이드라인에서는 기본 **Preset** 구성 요소에 대한 개요를 제공하고 XML을 기반으로 사전 설정 구성 파일에 이러한 구성 요소를 포함하는 방법을 설명합니다. 이후 섹션에서는 엄격한 구현 패턴에 따라 프리셋 파일의 다양한 구성 요소에 대해 설명합니다.

XML 구조는 <로 시작하고 >로 끝나는 마크업 구조인 **tags**를 기반으로 합니다. 결과 요소는 시작점과 끝점으로 정의되며, 시작 태그와 끝 태그 또는 빈 요소 태그의 조합으로 정의할 수 있습니다.

Presets는 ![](images/three-horizontal-icon.png){class="intxt-image"} > **Configuration** > **Result** > **Presets**에서 추가할 수 있으며, 이 워크플로(workflow)는 [preset brick]()을 만드는 것과 유사합니다. 사용자는 준비된 XML 파일을 업로드하거나 인라인 XML 편집기를 사용할 수 있습니다. 프리셋을 저장하면 구문 검사가 트리거됩니다.

*start-tab*와 *end-tag*의 **Example** 

```xml
<tagName tagAttributes="tagAttributeValue" >
    tagValue
</tagName>
```

*empty-element tab*의 **Example**

```xml
<tagName tagAttributes="tagAttributeValue" />
```

필요한 모든 구성은 하나의 **Preset** 파일에 정의하거나 소위 [preset bricks]()으로 정의되는 별도의 부분으로 하위 구조화할 수 있습니다.

##### Preset components

**Preset**을 조합하려면 구성 파일에 다음 태그 목록이 포함되어야 합니다. 이러한 태그 중 일부는 변경 가능한 특정 속성을 가지고 있으며 [여기]()에서 자세히 설명합니다.

:::{admonition} Required tags
:class: tip
- **preset**: preset의 래퍼 태그(wrapper tag), 다른 모든 태그는 이 요소 내에 있어야 합니다.
- **presetname**: presets을 선택할 때 표시되는 preset의 이름입니다.
- **presetversion**: preset의 버전
- **views**: 목록에 정의된 사용 가능한 다른 보기
- **list**: 목록은 특정 그리드 열 설정을 정의하며 presets의 기본 상위 태그입니다.
- **columns**: 모든 열의 래퍼 태그(wrapper tag)
- **column**: 그리드에 표시할 개별 열입니다.
- **scenario**: [시나리오 트리(scenario tree)]()를 정의합니다.
:::

Preset에 필요한 최소 XML의 **Example**:

```xml
<Preset>
    <presetname>TEST NAME</presetname>
    <presetversion>TEST VERSION</presetversion>
    <views default_listview="Default">
        <list name="Default">
            <columns>
                <column>
                </column>
            </columns>
        </list>
        <scenario name="Default">
            <root>
                <node name="Default"></node>
            </root>
        </scenario>
    </views>
</Preset>
```

Preset에 적용된 최소 필수 태그와 관련된 그리드 view입니다:

![alt text](images/grid-view.png)

##### Preset bricks

프리셋 브릭(Preset bricks)은 presets을 모듈화할 수 있는 도구입니다. 프리셋 브릭을 정의하는 것은 presets와 매우 유사하지만, 여러 presets 내에서 재사용 가능한 데이터의 하위 집합으로 사용할 수 있습니다.

프리셋 브릭 목록은 ![](images/three-horizontal-icon.png){class="intxt-image"} > **Configuration** > **Result** > **Preset Bricks**에서 액세스할 수 있습니다.

![alt text](images/preset-bricks.png)

##### Creating a new preset brick

프리셋 브릭(Preset bricks) 페이지에서 **New** 버튼을 클릭하면 새 프리셋 브릭을 만들 수 있는 화면으로 이동합니다.

![alt text](images/new-preset-brick.png)

프리셋 브릭(Preset bricks)에는 연락처와 파일 이름이 필요하며, 이는 파일 업로드 시 자동으로 설정되거나 사용자가 직접 설정해야 합니다. 파일 이름은 프리셋 브릭의 식별자와 동일합니다.

##### Adding a preset brick to a preset

다음 요소를 사용하면 프리셋 브릭(preset brick)이 **Preset**에 포함되며, 포함 요소의 위치는 프리셋 브릭과 프리셋에 지정된 열의 후속 위치를 정의합니다.

프리셋 브릭 NameOfPresetBrick.preset_brick을 프리셋 파일에 포함시키는 요소의 예시입니다.

```xml
<xi:include xmlns:xi="http://www.w3.org/2001/XInclude" href="NameOfPresetBrick.preset_brick" xpointer="xpointer(//brickid/*)"/>
```

##### Adding attributes to a preset

빈 열 태그(empty column tag) 안에 위의 기본 예제를 사용합니다. 그리드에 열이 될 테스트 속성을 다음과 같이 추가할 수 있습니다:

1. 속성 태그(attribute tag)를 만듭니다.
2. 속성 태그 안에 아이소코드 태그(isocode tag)를 만듭니다.
3. 표시하려는 속성 아이소코드를 아이소코드 태그에 추가합니다.

속성을 그리드 열로 추가한 XML 예시입니다.

```xml
<Preset>
    <presetname>TEST NAME</presetname>
    <presetversion>TEST VERSION</presetversion>
    <views default_listview="Default">
        <list name="Default">
            <columns>
                <column>
                    <attribute>
                        <isocode>meta.test.start_date</isocode>
                    </attribute>
                </column>
            </columns>
        </list>
        <scenario name="Default">
            <root>
            </root>
        </scenario>
    </views>
</Preset>
```

![alt text](images/resulting-grid-view-with-added-test-attribute.png)

시작 날짜가 대문자로 표시되지 않은 것을 확인한 사용자는 열 태그 내의 **lable tag** 속성을 활용하여 열에 대한 사용자 지정 레이블을 설정할 수 있습니다. 사전 설정된 XML이 변경되는 ![alt text](images/start-date-text.png)로 변경해 보겠습니다:

```xml
<Preset>
    <presetname>TEST NAME</presetname>
    <presetversion>TEST VERSION</presetversion>
    <views default_listview="Default">
        <list name="Default">
            <columns>
                <column label="Start Date">
                    <attribute>
                        <isocode>meta.test.start_date</isocode>
                    </attribute>
                </column>
            </columns>
        </list>
        <scenario name="Default">
            <root>
            </root>
        </scenario>
    </views>
</Preset>
```

![alt text](images/resulting-grid-view.png)

##### Adding nested attributes

빈 열 태그(empty column tag) 안에 위의 기본 예제를 사용하여 그리드의 열에 중첩된 속성을 추가할 수 있습니다:

1. 열 태그를 만들고 section 태그 속성을 true로 설정합니다.
2. 중첩된 열의 레이블 속성을 설정합니다.
3. 열 태그 내에서 위의 개별 열 추가 단계에 따라 원하는 만큼 중첩된 필드를 추가할 수 있습니다.
4. 중첩된 각 열 태그에 태그 속성 section = true가 포함되어 있는지 확인합니다.

중첩 열이 있는 프리셋 XML의 예시입니다.

```xml
<Preset>
    <presetname>Documentation Example</presetname>
    <presetversion>0.0.0</presetversion>
    <views default_listview="Default">
        <list name="Default">
            <columns>
                <column label="Start Date">
                    <attribute>
                        <isocode>meta.test.start_date</isocode>
                    </attribute>
                </column>
                <column section="true" label="B-Pillar">
                    <column section="true" decimals="2" label="Lower left">
                        <attribute>
                            <isocode>1.0.LE.R.O.VEHICLE_OLC_BPILLAR_LOWER_LEFT_VALUE_ELECTRICAL</isocode>
                        </attribute>
                    </column>
                    <column section="true" decimals="2" label="Lower right">
                        <attribute>
                            <isocode>1.0.RI.R.O.VEHICLE_OLC_BPILLAR_LOWER_RIGHT_VALUE_ELECTRICAL</isocode>
                        </attribute>
                    </column>
                </column>
            </columns>
        </list>
        <scenario name="Default">
            <root>
            </root>
        </scenario>
    </views>
</Preset>
```

그리드는 중첩된 열을 집계된 보기(aggregated view)로 표시합니다. 열 머리글(column header)은 > 를 클릭하여 확장하고 < 를 사용하여 다시 축소할 수 있습니다.

![alt text](images/expanded-preset-grid.png)

:::{admonition} Note
:class: tip
중첩된 필드는 추가로 중첩된 필드를 포함할 수 있으며 완전히 사용자 지정할 수 있습니다.
:::

##### Adding tables to a preset

Table은 프리셋 내에서 독립적인 그리드 구성을 정의할 수 있어 프리셋을 더욱 유연하게 만드는 데 사용됩니다. 예를 들어 하나의 프리셋 내에서 다양한 분야에 적용할 수 있습니다. 표는 그리드 사이드 패널에서 선택할 수 있습니다.

view 요소에 list 태그를 추가한 예시입니다.

```xml
<Preset>
    <presetname>TEST NAME</presetname>
    <presetversion>TEST VERSION</presetversion>
    <views default_listview="Default">
        <list name="Default">
            <columns>
                <column>
                </column>
            </columns>
        </list>
        <list name="Table 2">
            <columns>
                <column>
                </column>
            </columns>
        </list>
        <list name="Table 3">
            <columns>
                <column>
                </column>
            </columns>
        </list>
        <scenario name="Default">
            <root>
            </root>
        </scenario>
    </views>
</Preset>
```

##### Adding scenarios to a preset

시나리오 트리(scenario tree)에서 구조화할 수 있는 시나리오에 테스트를 할당할 수 있습니다. 따라서 사전 설정에서 시나리오를 적용하는 것은 사용자별 테스트 필터와 동일합니다. 시나리오의 정의 및 할당 조건은 테스트 속성을 기반으로 합니다.

시나리오는 사전 설정과 달리 루트 및 노드라는 두 가지 주요 태그로 구성됩니다. 시나리오 트리는 루트에 의해 캡슐화된 다음 가지가 있는 트리와 유사하게 노드로 구성됩니다. 하지만 시나리오는 조건 태그 속성을 사용하여 시나리오에 테스트를 표시할 특정 조건을 지정합니다.

프리셋에 노드를 추가하려면 빈 프리셋 템플릿으로 시작하세요.

1. scenario 요소와 root 요소 아래에 node 태그를 추가합니다.
2. 노드 요소에 name = {{EXAMPLE_NAME}} 태그 속성을 포함합니다.

프리셋에 있는 시나리오 정의의 예입니다.

```xml
<Preset>
<presetname>Documentation Example</presetname>
    <presetversion>0.0.0</presetversion>
    <views default_listview="Default">
        <list name="Default">
            <columns>
                <column>
                </column>
            </columns>
        </list>
        <scenario name="Default">
            <root>
                <node name="Base Node">
                </node>
            </root>
        </scenario>
    </views>
</Preset>
```

이제 시나리오 탭에 기본 노드가 표시됩니다. 시나리오 노드를 선택하거나 선택 취소하고 그리드에 표시할 테스트를 결정할 수 있습니다.

:::{admonition} Note
:class: tip
조건이 없는 노드를 포함하면 모든 테스트가 로드되고 표시됩니다.
:::

##### Adding conditions to scenario nodes

노드에 조건을 추가하려면 부울 논리 연산자를 사용해야 합니다. 조건은 테스트 속성 아이소코드(isocodes)를 기반으로 하며 해당 값에 따라 필터링하는 데 사용됩니다.

테스트 속성으로 기존 DIRECTIVE 아이소코드가 있고 테스트에 ECE R137, ECE R135 또는 ECE R127과 같은 DIRECTIVE 속성이 필요한 시나리오 노드 ECE의 예시입니다.

```xml
<Preset>
<presetname>Documentation Example</presetname>
    <presetversion>0.0.0</presetversion>
    <views default_listview="Default">
        <list name="Default">
            <columns>
                <column>
                </column>
            </columns>
        </list>
        <scenario name="Default">
            <root>
                <node name="ECE" condition="DIRECTIVE in ['ECE R137','ECE 
                R135', 'ECER127']">
                </node>
            </root>
        </scenario>
    </views>
</Preset>
```

['ECE R137','ECE R135','ECER127']은 규정 목록입니다. in 키워드는 목록 내에서 테스트 속성 DIRECTIVE가 있는지 확인합니다. 시나리오 노드 ECE가 선택되었다면 DIRECTIVE 값이 FMVSS 208이면 그리드에 표시되지 않습니다. DIRECTIVE 값이 ECE R137이면 그리드에 표시됩니다.

자세한 내용은 [Conditions]()을 참조하세요.

:::{admonition} Note
:class: tip
노드 태그는 매우 유연하고 중첩이 가능하므로 복잡한 시나리오를 모든 데이터 세트에 맞출 수 있습니다.
:::

##### Adding column functions

열 기능은 presets를 위한 고급 기능입니다. 열에 적용할 수 있는 스크립트를 작성할 수 있습니다.

열 함수(Column function)가 포함된 XML의 예입니다.

```xml
<Preset>
    <presetname>Documentation Example</presetname>
    <presetversion>0.0.0</presetversion>
    <views default_listview="Default">
        <list name="Default">
            <columns>
                <column label="Start Date">
                    <attribute>
                        <isocode>meta.test.start_date</isocode>
                    </attribute>
                </column>
                <column decimals="2" label="Lower left">
                    <attribute>
                        <isocode>1.0.LE.R.O.VEHICLE_OLC_BPILLAR_LOWER_LEFT_VALUE_ELECTRICAL</isocode>
                    </attribute>
                </column>
                <column decimals="2" label="Lower right">
                    <attribute>
                        <isocode>1.0.RI.R.O.VEHICLE_OLC_BPILLAR_LOWER_RIGHT_VALUE_ELECTRICAL</isocode>
                    </attribute>
                </column>
            </columns>
        </list>
        <scenario name="Default">
            <root>
                <node name="Base Node"></node>
            </root>
        </scenario>
    </views>
</Preset>
```

열 함수를 포함하려면 몇 가지 단계가 있습니다:

1. 함수를 적용하려는 열에 function_name 태그 속성이 있는 value_aggregation_config 태그를 추가합니다.

2. 마지막 목록 태그 아래에 추가합니다:

```xml
<column_functions>
    <column_function name="default_name">
            <code>
            </code>
    </column_function>
</column_functions>
```

column_functions 태그에 column_functions 태그를 더 추가하여 필요한 만큼 함수를 정의할 수 있습니다.

3. 위의 코드 태그에서 스크립트 기능을 추가할 수 있습니다.

이 예에서는 sum 열 함수를 만들었습니다. 위의 단계에 따라 예제 프리셋을 사용하면 기본 열의 중첩된 필드에 있는 값의 합계를 표시하는 sum 열 함수가 만들어집니다.

1단계 이후의 XML 예시

```xml
<Preset>
    <presetname>Documentation Example</presetname>
    <presetversion>0.0.0</presetversion>
    <views default_listview="Default">
        <list name="Default">
            <columns>
                <column label="Start Date" >
                    <attribute>
                        <isocode>meta.test.start_date</isocode>
                    </attribute>
                </column>
                <column decimals="2" label="Demo Function">
                    <value_aggregation_config function_name="sum"/>
                    <column decimals="2" label="Test One">
                        <attribute>
                            <isocode>0.0.00.D.O.GENERAL_INFORMATION_TEST_TEMPERATURE</isocode>
                        </attribute>
                    </column>
                    <column decimals="2" label="Test Two">
                        <attribute>
                            <isocode>0.0.00.D.O.GENERAL_INFORMATION_TEST_TEMPERATURE</isocode>
                        </attribute>
                    </column>
                </column>
            </columns>
        </list>
        <scenario name="Default">
            <root>
                <node name="Base Node"></node>
            </root>
        </scenario>
    </views>
</Preset>
```

2단계 이후의 XML 예시

```xml
<Preset>
    <presetname>Documentation Example</presetname>
    <presetversion>0.0.0</presetversion>
    <views default_listview="Default">
        <list name="Default">
            <columns>
                <column label="Start Date" >
                    <attribute>
                        <isocode>meta.test.start_date</isocode>
                    </attribute>
                </column>
                <column decimals="2" label="Demo Function">
                    <value_aggregation_config function_name="sum"/>
                    <column decimals="2" label="Test One">
                        <attribute>
                            <isocode>0.0.00.D.O.GENERAL_INFORMATION_TEST_TEMPERATURE</isocode>
                        </attribute>
                    </column>
                    <column decimals="2" label="Test Two">
                        <attribute>
                            <isocode>0.0.00.D.O.GENERAL_INFORMATION_TEST_TEMPERATURE</isocode>
                        </attribute>
                    </column>
                </column>
            </columns>
        </list>
        <column_functions>
            <column_function name="sum">
                <code>
                </code>
            </column_function>
        </column_functions>
        <scenario name="Default">
            <root>
                <node name="Base Node"></node>
            </root>
        </scenario>
    </views>
</Preset>
```

3단계 이후의 XML 예시

```xml
<Preset>
    <presetname>Documentation Example</presetname>
    <presetversion>0.0.0</presetversion>
    <views default_listview="Default">
        <list name="Default">
            <columns>
                <column label="Start Date" >
                    <attribute>
                        <isocode>meta.test.start_date</isocode>
                    </attribute>
                </column>
                <column decimals="2" label="Demo Function">
                    <value_aggregation_config function_name="sum"/>
                    <column decimals="2" label="Test One">
                        <attribute>
                            <isocode>0.0.00.D.O.GENERAL_INFORMATION_TEST_TEMPERATURE</isocode>
                        </attribute>
                    </column>
                    <column decimals="2" label="Test Two">
                        <attribute>
                            <isocode>0.0.00.D.O.GENERAL_INFORMATION_TEST_TEMPERATURE</isocode>
                        </attribute>
                    </column>
                </column>
            </columns>
        </list>
        <column_functions>
            <column_function name="sum">
                <code>scv_float = []
for v in scv:
    try:
        scv_float.append(float(v))
    except ValueError:
        pass

res = sum(scv_float) if scv_float else ""
                </code>
            </column_function>
        </column_functions>
        <scenario name="Default">
            <root>
                <node name="Base Node"></node>
            </root>
        </scenario>
    </views>
</Preset>
```

그리드에는 데모 함수 열의 테스트 1 및 테스트 2 열의 합계가 표시됩니다.

![alt text](images/demo-function-column.png)

root 열을 펼치면 열 값이 사용자에게 표시됩니다.

![alt text](expanded-demo-function-column.png)

### Add-ons

- [Add-ons overview](#add-ons-overview)
- [Adding a new add-on](#adding-a-new-add-on)
- [Editing add-ons](#editing-add-ons)
- [Periodic add-ons](#periodic-add-ons)

---

Add-ons은 기존 애플리케이션에 특정 기능 세트를 추가하기 위해 설치할 수 있는 소프트웨어 구성 요소입니다. 대표적인 예로는 웹 보고서, 타사 시스템에 대한 데이터 참조 또는 데이터 분석 애드온(Add-on)이 있습니다. 애드온은 타사에서 개발하여 애플리케이션 회사에서 독립적으로 제공할 수도 있습니다.

SCALE에서 개발한 애드온에 대한 개요는 애드온(Add-ons)에서 확인할 수 있습니다.

#### Add-ons overview

Add-on을 선택하기 위해 다음과 같이 진행합니다.

1. 상단 오른쪽 모서리의 ![](images/three-horizontal-icon.png){class="intxt-image"}를 클릭합니다. 
2. 나타나는 메뉴에서 **Configuration**을 클릭합니다.
3. configuration영역의 왼쪽 사이드 바에서 **Add-ons**를 클릭합니다. 사용 가능한 애드온들이 표시됩니다. 

![alt text](images/add-ons-overview.png)

한 줄을 클릭하면 추가 기능에 대한 자세한 상세 보기가 열리며, 기본 속성과 추가 정보를 확인할 수 있습니다. 

:::{admonition} Add-on properties
:class: tip
- **Schedule**: linear (>) 및 periodically ( ![alt text](images/periodically.png){class="intxt-images"} ) 실행되는 추가 기능의 아이콘을 표시합니다.
- **Name**: Add-on의 이름입니다.
- **Version**: 현재 시스템에 설치된 add-on의 버전 번호입니다.
- **Modified**: 마지막 수정 또는 업데이트 날짜
- **Type**: Add-on을 실행할 수 있는 컨텍스트에 대한 정보(다음 옵션을 포함)입니다:
    - **Browser Add-on**: 이 유형의 add-on은 브라우저 애플리케이션에 더 많은 기능을 추가합니다. 이 유형의 add-on은 모든 데스크톱 설치에서도 사용할 수 있습니다.
    - **Desktop Add-on**: 이 추가 기능은 애플리케이션이 데스크톱 클라이언트에서 실행 중인 경우에만 표시됩니다.
- **Next Execution**: add-on의 다음 실행 예정 날짜 및 시간입니다. 현재 add-on이 정기 add-on으로 표시된 경우에만 표시됩니다. 자세한 내용은 [Periodic Add-ons](#periodic-add-ons)을 참조하세요.
- **Status**: 토글 스위치로 add-on을 활성화 또는 비활성화할 수 있습니다.
:::

![alt text](images/add-ons-detail-view.png)

헤더(header)에서 토글 스위치를 사용하여 add-on을 활성화 및 비활성화할 수 있습니다. 강조 표시된(highlighted) 배경(background)은 add-on이 활성화되어 사용자에게 표시됨을 나타냅니다. 토글 아이콘이 회색으로 표시되어 있으면 add-on이 현재 비활성화된 상태이며 애플리케이션에서 사용할 수 없습니다. ![alt text](images/download-add-on.png){class="intxt-images"}를 클릭하면 add-on을 다운로드할 수 있고, ![alt text](images/remove-icon.png){class="intxt-images"}를 클릭하면 add-on을 삭제할 수 있습니다.

add-on에 대한 정보는 다음과 같습니다:

:::{admonition} Add-on information
:class: tip
- **Description**: add-on의 목적과 기능을 포함한 add-on에 대한 간략한 개요입니다. 특정 add-on의 기능이 무엇인지 잘 모르겠다면 여기에서 자세한 정보를 확인할 수 있습니다.
- **Modification Date**: add-on을 마지막으로 수정하거나 업데이트한 날짜와 시간입니다.
- **Type**: 브라우저 또는 데스크톱 add-on를 구분합니다.
- **Version**: 현재 시스템에 설치된 add-on의 버전 번호입니다.
- **Next Execution**: add-on의 다음 실행 예정 날짜 및 시간입니다. 현재 add-on이 정기(periodic) add-on으로 표시된 경우에만 표시됩니다. 자세한 내용은 [Periodic Add-ons](#periodic-add-ons)을 참조하세요.
:::

_Properties_ 패널 아래에는 두 개의 추가 패널이 있습니다:

- _History_: 이 패널에서는 수정 날짜 및 시간, 수정한 사용자, 수정에 대한 간략한 설명을 포함하여 add-on에 대한 모든 변경 사항에 대한 자세한 개요를 제공합니다.
- _Changelogs_: 변경 로그는 시스템 또는 소프트웨어에 대한 모든 변경, 업데이트 및 개선 사항을 문서화한 기록입니다. add-on과 관련하여 발생한 모든 변경사항에 대한 개요를 제공하기 위해 여기에 표시됩니다.

#### Adding a new add-on

[add-ons overview](#add-ons-overview)의 하단 오른쪽 모서리에 ![](images/black-plus.png){class="intxt-image"}를 클릭하여 새 add-on을 추가 합니다.

![alt text](images/add-new-add-on-view.png)

1. ![alt text](images/upload-icon.png){class="intxt-image"} **Upload new File**를 클릭하여 .zip 파일을 업로드 합니다.
2. 추가적으로 다음의 속성을 정의할 수 있습니다. 

:::{admonition} Add-on properties
:class: tip
- **Restrictions** - _optional_ - add-on이 연결되고 액세스할 수 있는 애플리케이션 [presets]()을 여러 개 선택할 수 있습니다.
- **Contact Data** - _mandatory_ - **Person** 모델의 개체가 있는 드롭다운 메뉴 입니다.
:::

3. add-on 파일을 업로드 하고 속성을 설정한 후에 ![](images/save-icon.png){class="intxt-image"}를 클릭하여 add-on을 추가합니다.
4. **X**를 클릭하면 add-on 추가는 취소되고 다시 [add-ons overview](#add-ons-overview)로 돌아갑니다.

:::{admonition} Bad add-on file
:class: caution
만약 유효한 .zip add-on 파일이 아니라면 애플리케이션은 업로드은 취소되며 새 add-on은 설치되지 않습니다. 이럴 경우 add-on 공급자에게 문의하고 올바른 add-on 파일이 업로드 되도록 하세요.
:::

#### Editing add-ons

이미 설치된 add-on을 편집하려면 add-on의 상세 보기에서 **circle pen**을 클릭합니다. add-on을 편집하는 것은 새 add-on을 추가하는 것과 거의 동일합니다. 그러면 새 add-on 파일을 업로드하고, 일정을 변경하고, 사전 설정된 제한을 설정하고, 담당자를 지정할 수 있는 편집 페이지로 이동합니다.

#### Periodic add-ons

업로드한 add-on이 주기적으로 실행되도록 하려면 **circle pen**을 클릭하면 추가 일정 섹션을 표시합니다. 목록에서 원하는 시간과 요일을 선택하여 간단한 주간 일정을 설정할 수 있습니다. 보다 복잡한 일정이 필요한 경우에는 **Use crontab syntax** 버튼을 사용하여 crontab 구문을 사용하여 사용자 지정 일정을 설정할 수 있습니다.

![alt text](images/schedule-for-periodic-execution-of-add-ons.png)

crontab 구문은 각 시간 옵션마다 분, 시간, 요일, 월, 요일 등 다섯 개의 입력 필드를 필요로 합니다.

:::{admonition} Caution
:class: caution
crontab 구문을 사용하여 사용자 지정 일정을 설정할 때는 각 필드의 값을 올바르게 입력하는 것이 중요하다는 점에 유의하세요. 잘못된 값을 입력하면 애드온이 원하는 시간에 실행되지 않거나 아예 실행되지 않을 수 있습니다.
:::

:::{admonition} Periodic settings
:class: tip
- **Minutes**: [0-59] - 명령이 실행되어야 하는 시간의 분을 나타냅니다.
- **Hours**: 시: [0-23] - 명령이 실행되어야 하는 하루 중 시간을 나타냅니다.
- **Day of the month**: [1-31] - 명령이 실행되어야 하는 월의 요일을 나타냅니다.
- **Month**: [1-12] 또는 월 이름(예: "Jan" 또는 "February") - 명령이 실행되어야 하는 월을 나타냅니다.
- **Day of the week**: [0-7] 또는 요일 이름(예: "Sun" 또는 "Monday", 여기서 0과 7은 모두 일요일을 나타냄) - 명령이 실행되어야 하는 요일을 나타냅니다.
:::

각 입력 필드에는 각각 으로 구분하여 여러 옵션을 포함할 수 있습니다. 예를 들어 분 필드에 0, 15, 30, 45를 입력하면 1시간의 1/4마다 작업이 수행됩니다.

다음 실행 필드에는 입력에 따라 다음 세 번의 실행이 표시됩니다. 이 필드를 사용하여 일정이 예상과 일치하는지 확인할 수 있습니다.

:::{admonition} Caution
:class: caution
실행 일정을 너무 자주 설정하면 작업 대기열이 백업되는 문제가 발생하여 시스템 성능에 영향을 미치고 다른 작업을 실행하는 데 방해가 될 수 있습니다. 새 작업을 시작하기 전에 시스템이 작업을 완료할 충분한 시간을 확보할 수 있도록 부가 기능의 실행 시간보다 짧은 일정을 설정하지 않는 것이 중요합니다.
:::

### User management

**User management** 메뉴에서는 사용자 계정, 그룹, 글로벌 역할, 프로젝트 역할을 만들 수 있습니다.

1. 상단 오른쪽 모서리의 ![](images/three-horizontal-icon.png){class="intxt-image"}를 클릭합니다.
2. **Configuration**을 선택합니다.
3. 왼쪽 메뉴에서 **User management**를 클릭하고 다음에서 원하는 항목을 선택합니다.
    - [Users](#users)
    - [Groups](#groups)
    - [Access tokens](#access-tokens)
    - [Global roles](#global-roles)
    - [Project roles](#project-rol)

---

#### Users

**Users** 보기에서는 시스템의 모든 사용자 계정에 대한 개요를 제공합니다. 화면 상단의 필터를 사용하여 특정 사용자를 검색할 수 있습니다.

![alt text](images/overview-of-all-users.png)

##### Create or edit a user account

1. **Configuration** > **User management** > **Users**로 이동합니다.
2. 기존 사용자 계정을 수정하거나 삭제하려면 개요에서 해당 사용자를 클릭합니다. 새 사용자 계정을 만들려면 오른쪽 상단 모서리에서 **New**를 클릭합니다.
3. 필요에 따라 설정을 구성합니다. 각 설정에 대한 설명은 아래에 나와 있습니다.
4. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다.

![alt text](images/create-or-edit-a-user-account.png)

:::{list-table}
:widths: 15 100
:header-rows: 1

*   - Setting
    - Explanation    
*   - ![](images/remove-icon.png){class="intxt-image"}
    - 사용자를 삭제하려면 이 아이콘을 클릭합니다.
    **Caution**: 이렇게 하면 데이터베이스에서 사용자 개체가 영구적으로 제거됩니다. 일시적으로 로그인을 금지해야 하는 경우 **General information** 섹션까지 아래로 스크롤하여 **Active** 설정 옆의 확인 표시를 제거합니다.
*   - **User name**
    - 인증 페이지의 로그인 이름입니다. 사용자 이름은 다음 요구 사항을 충족해야 합니다:
        - 150자 이하.
        - 문자, 숫자 및 @ . + - _         
        참고: 사용자 아이디가 변경되면 현재 자격 증명이 더 이상 유효하지 않으므로 사용자는 다시 로그인해야 합니다.
*   - **Internal**
**External**
    - 사용자 이름 옆에는 사용자가 내부 사용자인지 외부 사용자인지를 나타내는 칩(chip)이 있습니다.
        - **Internal**: 사용자 이름, 이메일, 표시 이름 등의 정보를 수정할 수 있습니다.
        - **External**: 사용자와 해당 정보는 외부 ID 공급업체에서 가져온 것입니다. 따라서 사용자 이름, 이메일, 표시 이름 등의 정보는 편집할 수 없습니다.
*   - **Change pasword**
    - 사용자의 비밀번호를 변경하려면 이 버튼을 클릭합니다. 비밀번호는 다음 요건을 충족해야 합니다:
        - 다른 개인정보와 유사하지 않아야 합니다.
        - 일반적으로 사용하는 비밀번호가 아닐 수 있습니다.
        - 8자 이상이어야 합니다.
        - 숫자와 문자를 모두 포함해야 합니다.        
        참고: 비밀번호가 변경되면 현재 자격 증명이 더 이상 유효하지 않으므로 사용자는 다시 로그인해야 합니다.
:::

###### Users: Personal information

여기에서는 사용자의 이메일 주소와 표시되는 이름을 수정 할 수 있습니다. 

![alt text](images/personal-information.png)

:::{list-table}
:widths: 15 100
:header-rows: 1
*   - Setting
    - Explanation
*   - **E-mail**
    - 사용자의 이메일 주소
*   - **Display name**(mandotory)
    - SCALE.sdm 전체에 걸쳐 여러 영역에 표시되는 이름입니다. 예를 들어 표시되는 이름은 ![](images/project-icon.png){class="intxt-image"} **프로젝트**의 requirements 그리드에 표시됩니다. 표시되는 이름은 사용자 이름이 모호한 경우에 특히 유용합니다. 예를 들어 사용자 이름이 johnny417이고 표시되는 이름이 John Doe라고 가정해 보겠습니다. 사용자는 johnny417로 로그인하지만 ![](images/project-icon.png){class="intxt-image"} **프로젝트**에서 requirement의 상태를 변경한 사용자로 John Doe가 표시됩니다.
:::

###### Users: General information

여기에서는 애플리케이션 내에서 사용자의 권한과 역할을 추가로 정의할 수 있습니다.

![alt text](images/general-information.png)

:::{list-table}
:widths: 15 100
:header-rows: 1
*   - Setting
    - Explanation
*   - **Active**
    - 사용자 계정을 삭제하지 않고 비활성 상태로 표시할 수 있습니다:
        - 이 옵션을 선택(![](images/check-box-icon.png){class="intxt-image"})하면 해당 사용자는 활성 상태로 처리됩니다.
        - 이 옵션을 선택하지 않으면 해당 사용자는 비활성으로 처리됩니다. 즉, 사용자는 로그인할 수 없게 됩니다.
*   - **Staff**
    - 이 옵션을 선택(![](images/check-box-icon.png){class="intxt-image"})하면 사용자가 관리자 영역에 접근할 수 있습니다.
*   - **Superuser**
    - 이 옵션이 선택(![](images/check-box-icon.png){class="intxt-image"})하면 명시적으로 권한을 할당 할 필요 없이 사용자에게 모든 권한이 부여됩니다.
*   - **Disciplines**
    - 드롭다운 목록을 열고 사용자가 속한 모든 분야를 선택합니다. 이렇게 하면 사용자가 액세스할 수 있는 리소스가 제어됩니다.
*   - **Layout**
    - 드롭다운 목록을 열고 사용자를 위한 프런트엔드(frontend) 레이아웃을 선택합니다. 고정형(fixed)과 유동형(fluid)의 두 가지 옵션이 있습니다. 고정 레이아웃은 1280px의 창 너비에 맞게 구성됩니다.
:::

###### Users: Active personal access tokens

여기에서 자신의 활성 액세스 토큰(active access tokens)을 확인할 수 있으며 필요한 경우 토큰을 삭제할 수 있습니다.

![alt text](images/active-personal-access-tokens.png)

###### Users: Permissions

대부분의 사용자 권한은 일반적으로 사용자에게 할당된 [역할](#users-roles)을 통해 설정됩니다. 그러나 예외적인 경우에는 개별 사용자에게 추가 권한을 할당할 수 있습니다. 사용자 권한 집합은 사용자의 역할과 관련된 모든 권한과 해당 사용자에 대해 특별히 정의된 모든 권한의 조합으로 결정됩니다.

![alt text](images/user-permissions.png)

![alt text](images/permission-graph.png)

###### Users: Roles

여기에서 사용자에게 역할을 할당할 수 있습니다.

참고: 역할은 **Configuration** > **User management** > **Global roles**에서 이미 만들어져 있어야 합니다. 글로벌 역할을 만드는 방법은 [여기](#global-roles)에서 확인할 수 있습니다.

![alt text](images/user-roles.png)

###### Users: Groups

여기에서 사용자에게 그룹을 할당할 수 있습니다.

참고: 그룹은 **Configuration** > **User management** > **Groups**에서 이미 만들어져 있어야 합니다. 그룹을 만드는 방법은 [여기](#groups)에서 확인할 수 있습니다.

![alt text](images/user-groups.png)

##### Groups

**Groups** 보기에서는 시스템의 모든 그룹에 대한 개요를 제공합니다.

![alt text](images/overview-of-all-groups.png)

###### Create or edit a group

1. **Configuration** > **User management** > **Groups**으로 이동합니다.
2. 기존 그룹을 수정하거나 삭제하려면 개요에서 해당 그룹을 클릭합니다. 새 그룹을 만들려면 오른쪽 상단 모서리에 있는 **New**를 클릭합니다.
3. 필요에 따라 설정을 구성합니다. 각 설정에 대한 설명은 아래에 나와 있습니다.
4. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다.

![alt text](images/create-or-edit-a-group.png)

:::{list-table}
:widths: 15 100
:header-rows: 1
*   - Setting
    - Explanation
*   - ![](images/remove-icon.png){class="intxt-image"}
    - 그룹을 삭제하기 위해 이 아이콘을 클릭합니다.
*   - **Name**(mandotory)
    - 사용자 그룹의 이름입니다.
*   - **Permissions**
    - [Permissions](#users-permissions)는 사용자에게 할당되는 것과 동일한 방식으로 그룹에 할당됩니다.
*   - **Roles**
    - [Roles](#users-roles)은 사용자에게 할당되는 것과 동일한 방식으로 그룹에 할당됩니다.
*   - **Users**
    - 그룹 권한은 그룹 구성원에게 상속됩니다.
:::

#### Access tokens

**Access tokens** 보기에서는 시스템의 모든 액세스 토큰에 대한 개요를 제공합니다. 액세스 토큰에 대한 자세한 정보와 개인용 액세스 토큰을 만드는 방법은 [여기]()에서 확인할 수 있습니다.

#### Global roles

글로벌 역할(global roles)은 ![](images/project-icon.png){class="intxt-image"}**Project**와 ![](images/result-icon.png){class="intxt-image"}**Result** 모두에서 사용되는 프로젝트 독립적인 권한 집합입니다. [여기]()에서 글로벌 역할을 보고 관리할 수 있습니다.

##### View a global role

글로벌 역할(global roles)에 대해 어떤 권한이 설정되어 있는지 확인할 수 있습니다. 권한은 사이드 패널의 읽기 전용 권한 트리에 표시됩니다.

1. ![](images/three-horizontal-icon.png){class="intxt-image"} > **Configuration** > **User management** > **Global roles**로 이동합니다.
2. 개요에서 역할을 클릭한 다음 ![](images/double-left-arrow.png){class="intxt-image"} 클릭하여 사이드 패널을 펼칩니다.
3. 선택 사항: 검색 및 필터 옵션을 사용하여 권한 목록을 찾아봅니다.

![alt text](images/side-panel-for-role-permissions.png)

:::{admonition} Side panel is visible depending on permissions
:class: tip
사이드 패널(side panel)은 보기 권한이 있는 사용자 및 역할 변경 권한이 있는 사용자가 액세스할 수 있습니다. 그러나 사이드 패널의 권한 트리는 항상 읽기 전용으로 표시됩니다. 즉, 편집 권한이 있는 사용자라도 사이드 패널에서 권한을 편집할 수 없습니다. 편집하려면 편집 페이지(edit page)로 이동해야 합니다.
:::

##### Create or edit a golbal role

1. ![](images/three-horizontal-icon.png){class="intxt-image"} > **Configuration** > **User management** > **Global roles**로 이동합니다.
2. 기존 글로벌 역할(global roles)을 수정하려면 개요에서 ![alt text](images/pencil-in-box.png){class="intxt-image"} 아이콘을 클릭합니다. 기존 글로벌 역할을 삭제하려면 개요에서 ![](images/remove-icon.png){class="intxt-image"} 아이콘을 클릭합니다. 새 글로벌 역할을 만들려면 오른쪽 상단 모서리에 있는 **New**를 클릭합니다.
3. 필요에 따라 설정을 구성합니다. 각 설정에 대한 설명은 아래에 나와 있습니다.
4. ![](images/save-icon.png){class="intxt-image"}를 클릭하여 설정을 저장합니다.

![alt text](images/create-or-edit-a-globa-role.png)

:::{list-table}
:widths: 15 100
:header-rows: 1

*   - Setting
    - Explanation    
*   - **Role name** (mandatory)
    - 글로벌 역할(global roles)의 이름
    
*   - **Is default**
    - 이 옵션을 선택(![](images/check-box-icon.png){class="intxt-image"})하면 새로 만든 모든 사용자에게 이 역할이 적용됩니다.        
*   - **Permissions**
    - [권한](#users-permissions)은 사용자에게 할당되는 것과 동일한 방식으로 글로벌 역할에 할당됩니다.
:::

#### Project roles

글로벌 역할(global roles)과 달리 프로젝트 역할(project roles)은 프로젝트 내에서 [프로젝트 구성원](#project-members)에게 할당되는 역할이며 프로젝트별 요구 사항에 따라 정의할 수 있습니다. 여기에서 프로젝트 역할을 보고 관리할 수 있습니다.

![alt text](images/overview-of-all-project-roles.png)

##### Create or edit a project role

1. ![](images/three-horizontal-icon.png){class="intxt-image"} > **Configuration** > **User management** > **Project roles**로 이동합니다.
2. 기존 프로젝트 역할(project roles)을 편집하려면 개요에서 ![](images/pencil-in-box.png){class="intxt-image"} 아이콘을 클릭합니다. 기존 프로젝트 역할을 삭제하려면 개요에서 ![](images/remove-icon.png){class="intxt-image"} 아이콘을 클릭합니다. 새 프로젝트 역할을 만들려면 오른쪽 상단 모서리에 있는 **New**를 클릭합니다.
3. 필요에 따라 설정을 구성합니다. 각 설정에 대한 설명은 아래에 나와 있습니다.
4. ![](images/save-icon.png) 를 클릭하여 설정을 저장합니다.

![alt text](images/create-or-edit-a-project-role.png)

:::{list-table}
:widths: 15 100
:header-rows: 1

*   - Setting
    - Explanation    
*   - **Role name** (mandatory)
    - 프로젝트 역할(project roles)의 이름
*   - **Permissions**
    - [권한](#users-permissions)은 사용자에게 할당되는 것과 동일한 방식으로 프로젝트 역할에 할당됩니다.
:::

#### Permissions


### Announcements
### Jobs