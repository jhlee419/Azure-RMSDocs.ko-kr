![빠른 시작 자습서 1단계](../media/AzRMS_QuickStartSteps1.PNG)

Azure Rights Management를 지원하는 구독이 있는 경우라도 서비스는 기본적으로 비활성화되어 있습니다. 서비스를 활성화하려면 Office 365 관리 센터 또는 Azure 클래식 포털을 사용하면 됩니다.

-   Azure 권한 관리가 포함된 Office 365 구독이 있거나, Azure 권한 관리가 제외된 Office 365 구독을 사용하지만 Azure RMS Premium 구독이 있는 경우: **Office 365 관리 센터를 사용**합니다.

-   Office 365 구독이 없는 경우: **Azure 클래식 포털을 사용**합니다.

![Azure 클래식 포털](../media/AzRMS_Tutorial_1_Screenshots.png)

#### <a name="to-activate-rights-management-from-the-office-365-admin-center"></a>Office 365 관리 센터에서 권한 관리를 활성화하려면

1.  [Office 365 포털](https://portal.office.com/)로 이동하여 회사 또는 학교 계정으로 로그인합니다.

2.  Office 365 관리 센터가 자동으로 표시되지 않으면 왼쪽 위에서 앱 시작 관리자 아이콘을 선택하고 **관리자**를 선택합니다. **관리자** 타일은 Office 365 관리자에게만 나타납니다.

    > [!TIP]
    > 관리 센터 도움말은 [Office 365 관리 센터 정보 - 관리자 도움말](https://support.office.com/article/About-the-Office-365-admin-center-Admin-Help-58537702-d421-4d02-8141-e128e3703547)을 참조하세요.

3.  왼쪽 창에서 **서비스 설정**을 확장합니다.

4.  **권한 관리**를 클릭합니다.

5.  **권한 관리** 페이지에서 **관리**를 클릭합니다.

6.  **Rights Management** 페이지에서 **활성화**를 클릭합니다.

7.  **권한 관리를 활성화하시겠나요?**라는 메시지가 나타나면 **활성화**를 클릭합니다.

이제 **Rights Management가 활성화된** 것을 확인하고 비활성화할 수 있습니다(페이지를 수동으로 새로 고쳐야 할 수 있음).

이때 **고급 기능**을 클릭하지 마세요. 템플릿을 구성하는 Azure 클래식 포털로 이동할 수 있지만 이 자습서에서는 이 기능이 필요하지 않습니다. 대신 Office 365 관리 센터를 닫을 수 있습니다.

#### <a name="to-activate-rights-management-from-the-azure-portal"></a>Azure 포털에서 Rights Management를 활성화하려면

1.  [Azure 클래식 포털](http://go.microsoft.com/fwlink/p/?LinkID=275081)로 이동하여 로그인합니다.

2.  왼쪽 창에서 **ACTIVE DIRECTORY**를 클릭합니다.

3.  **Active Directory** 페이지에서 **Rights Management**를 클릭합니다.

4.  [!INCLUDE[aad_rightsmanagement_2](../includes/aad_rightsmanagement_2_md.md)]에 대해 관리할 디렉터리를 선택하고 **활성화**를 클릭한 다음 작업을 확인합니다.

이제 **Rights Management 상태** 가 **활성** 으로 표시되고 **활성화** 옵션이 **비활성화**로 바뀝니다.

포털에서 Rights Management에 대한 다른 옵션을 구성할 수 있지만, 이 자습서에서는 필요하지 않으므로 Azure 클래식 포털을 닫을 수 있습니다.

이 첫 번째 단계는 그 정도로 충분합니다. 서비스가 활성화되어 이제 조직에 있는 모든 사용자가 중요한 문서를 보호하기 시작할 수 있습니다. 프로덕션 환경에서는 단계적인 배포를 위해 처음에 이 작업을 수행할 수 있는 사람을 제한하는 것이 좋습니다. 하지만 이 자습서에서는 그럴 필요가 없습니다.

여기에는 포함되어 있지 않지만, 프로덕션 배포에서는 사용자 지정 템플릿도 구성하는 것이 좋습니다. 템플릿을 구성하면 사용자가 파일을 보호해야 할 때 올바른 설정을 빠르게 적용할 수 있습니다. Rights Management를 활성화하면 2개의 기본 템플릿을 자동으로 받으며, 프로덕션 환경에서는 여기에 추가로 사용자 지정 템플릿을 만들어 보충하는 것이 좋습니다. 그러나 이 자습서에서는 템플릿이 필요하지 않으므로 다음 단계로 이동하면 됩니다.

|자세한 정보가 필요한 경우|추가 정보|
|--------------------------------|--------------------------|
|Rights Management 활성화와 서비스가 활성화되었을 때 파일과 메일을 보호할 수 있는 사람의 제어에 관한 정보   →|[Azure 권한 관리 활성화](../deploy-use/activate-azure-classic.md)|
|기본 템플릿과 사용자 지정 템플릿을 새로 만드는 방법 정보   →|[Azure 권한 관리용 사용자 지정 템플릿 구성](../deploy-use/create-template.md)|
