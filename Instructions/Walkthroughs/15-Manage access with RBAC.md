---
wts:
    title: '15 - RBAC를 통한 접근 제어'
    module: '모듈 03 - 보안, 개인정보보호, 규정준수, 신뢰'
---

# 15 - RBAC를 통한 접근 제어

이 연습에서는 역할을 할당하고 활동 로그를 확인합니다.

실습 시간: 15 분

# 실습 1: 역할 보기와 할당

이 실습에서는 가상 머신에 기여자 역할을 지정합니다.

1. <a href="https://portal.azure.com" target="_blank"><span style="color: #0066cc;" color="#0066cc">Azure Portal</span></a>에 로그인 합니다.

2. 검색창에 **리소스 그룹**을 검색하고 **+추가**를 클릭합니다.

3. 다음을 이용하여 새로운 리소스 그룹을 생성합니다.

    | 설정 | 값 |
    | -- | -- |
    | 구독 | **실습에 이용할 구독**|
	| 리소스 그룹 | **myRGRBAC** |
    | 영역 | **(아시아 태평양)아시아 남동부** |
    | | |

4. **검토 + 만들기** 버튼을 클릭하고 **만들기** 버튼을 클릭합니다..

5. **리소스 그룹으로 이동** 버튼을 클릭하거나 리소스 그룹 블레이드에서 **새로 고침**을 클릭합니다.

6. **액세스 제어(IAM)**를 클릭하고 **역할** 탭을 클릭합니다. 미리 정의된 기본 역할 목록을 보고 정보 아이콘을 사용하여 각 역할의 권한에 대해 확인합니다. 각 역할에 할당 된 사용자 및 그룹 수에 대한 정보도 있습니다.

    ![생성된 리소스 그룹 블레이드에서 액세스 제어(IAM)과 역할이 강조 된 스크린 샷](../images/1501.png)

7. 메뉴 상단에 있는 **+ 추가**를 클릭하고 **역할 할당 추가**를 클릭하여 합니다. 자신을 가상 머신 참여자로 지정하고 **저장**을 클릭합니다.

    | 설정 | 값 |
    | -- | -- |
    | 역할 | **가상 머신 참여자** |
    | 다음에 대한 액세스 할당 | **Azure AD 사용자, 그룹 또는 서비스 보안 주체** |
    | 선택 | **자신의 계정** |
    | | |

    **메모**: 가상 머신 참여자 역할을 사용하면 가상 머신을 관리 할 수 ​​있지만 가상 머신에 연결된 스토리지 계정 또는 네트워크에는 액세스 할 수는 없습니다.

    ![액세스 제어(IAM) 블레이드에서 역할 추가를 하는 스크린 샷](../images/1502.png)


5. 역할 할당 페이지를 **새로 고침** 하고 사용자 계정이 가상 머신 참여자로 표시되는지 확인합니다.

**메모**: 가상 머신 참여자는 리소스 그룹에서 가상 머신을 관리 할 수 ​​있습니다. 가상 네트워크 또는 스토리지 계정에 액세스하는 것은 포함되지 않습니다. 

# 실습 2: 역할 할당 모니터링 및 역할 제거

이 실습에서는 활동 로그를 보고 역할 할당을 확인한 다음 역할을 제거합니다.

1. Azure portal에서 **활동 로그**를 탐색합니다.

2. **필터 추가**를 클릭하고 리소스에 **작업**, 0개 선택됨에 **역할 할당 만들기**를 선택합니다.

    ![활동 로그에 필터 추가를하여 작업과 역할 할당 만들기를 강조 한 스크린 샷](../images/1503.png)

3. 활동 로그에 역할 할당이 표시되는지 확인합니다.

4. 역할 할당을 제거하는 방법을 알고 있습니까?

역할을 할당하고 활동 로그를 확인해 보았습니다.

**메모**: 추가 비용을 피하기 위해 리소스 그룹을 제거할 수 있습니다. 리소스 그룹(myRGRBAC)을 검색하고 리소스 그룹 블레이드에서 **Delete resource group**을 클릭한 후 삭제 창에 리소스 그룹 이름 입력란에 리소스 그룹 이름(myRGRBAC)을 입력합니다. 리소스 그룹 이름을 정확히 입력하면 하단에 **삭제** 버튼이 활성화 되며 삭제 버튼을 클릭하여 생성한 리소스들을 삭제합니다. **알람**에서 모니터링 할 수 있습니다.
