---
# required metadata

title: Azure 권한 관리 커넥터 배포 | Azure RMS
description:
keywords:
author: cabailey
manager: mbaldwin
ms.date: 04/28/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: 90e7e33f-9ecc-497b-89c5-09205ffc5066

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: esaggese
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Azure 권한 관리 커넥터 배포
다음 정보를 통해 Azure 권한 관리(RMS) 커넥터와 이러한 커넥터를 사용하여 Microsoft Exchange Server, Microsoft SharePoint Server 또는 Windows Server를 실행하고 파일 서버 리소스 관리자의 FCI(파일 분류 인프라) 기능을 활용하는 파일 서버를 사용하는 기존 온-프레미스 배포에 정보 보호 기능을 제공하는 방법을 확인할 수 있습니다.

> [!TIP]
> 개괄적인 예제 시나리오 및 스크린샷을 보려면 [Azure RMS 실행](../understand-explore/what-admins-users-see.md) 문서에서 [Windows Server 및 파일 분류 인프라가 실행되는 파일 서버에서 파일을 자동으로 보호](../understand-explore/what-admins-users-see.md#automatically-protecting-files-on-file-servers-running-windows-server-and-file-classification-infrastructure) 섹션을 참조하세요.

## Microsoft Rights Management 커넥터 개요
Microsoft Rights Management(RMS) 커넥터를 통해 신속하게 기존 온-프레미스 서버가 클라우드 기반 Microsoft Rights Management 서비스(Azure RMS)에 IRM(정보 권한 관리) 기능을 사용하도록 할 수 있습니다. 이 기능을 통해 IT 및 사용자는 추가 인프라를 설치하거나 다른 조직과의 트러스트 관계를 설정할 필요 없이 조직 내/외부에서 쉽게 문서와 사진을 보호할 수 있습니다. 하이브리드 시나리오에서 일부 사용자가 온라인 서비스에 연결하더라도 이 커넥터를 사용할 수 있습니다. 예를 들어 일부 사용자의 사서함은 Exchange Online을 사용하고 일부 사용자의 사서함은 Exchange Server를 사용합니다. RMS 커넥터를 설치한 후에 모든 사용자는 Azure RMS를 사용하여 전자 메일 및 첨부 파일을 보호하고 사용할 수 있으며 정보 보호는 두 배포 구성 간에 원활하게 작동합니다.

RMS 커넥터는 Windows Server 2012 R2, Windows Server 2012 또는 Windows Server 2008 R2를 실행하는 서버에 온-프레미스로 설치하는, 사용 공간이 작은 서비스입니다. 물리적 컴퓨터에서 커넥터를 실행하는 것 외에도 Azure IaaS VM을 포함하여 가상 컴퓨터에서 실행할 수 있습니다. 이 커넥터를 설치 및 구성하고 나면 이 커넥터는 온-프레미스 서버와 클라우드 서비스 사이에서 통신 인터페이스(릴레이) 역할을 합니다.

Azure RMS에 대해 사용자 고유의 테넌트 키를 관리하는 경우('Bring You Own Key' 또는 BYOK 시나리오) RMS 커넥터 및 이 커넥터를 사용하는 온-프레미스 서버는 사용자의 테넌트 키가 포함된 HSM(하드웨어 보안 모듈)에 액세스하지 않습니다. 테넌트 키를 사용하는 모든 암호화 작업은 온-프레미스가 아니라 Azure RMS에서 수행되기 때문입니다.

![](../media/RMS_connector.png)

RMS 커넥터는 Exchange Server, SharePoint Server 및 Windows Server를 실행하고 파일 분류 인프라를 사용하여 Office 정책을 분류하고 폴더의 문서에 적용하는 파일 서버와 같은 온-프레미스 서버를 지원합니다. 파일 분류를 사용하여 모든 파일 형식을 보호하려는 경우 RMS 커넥터를 사용하지 않는 대신 [RMS 보호 cmdlet](https://msdn.microsoft.com/library/azure/mt433195.aspx)를 사용합니다.

> [!NOTE]
> 이러한 온-프레미스 서버의 지원되는 버전은 [Azure RMS를 지원하는 온-프레미스 서버](..\get-started\requirements-servers.md)를 참조하세요.

다음 정보를 참조하여 RMS 커넥터를 계획, 설치 및 구성할 수 있습니다. 그런 다음 서버가 커넥터를 사용할 수 있도록 설치 후 구성을 수행해야 합니다.

-   [RMS 커넥터의 사전 요구 사항](deploy-rms-connector.md#prerequisites-for-the-rms-connector)

-   **1단계:** [RMS 커넥터 설치](install-configure-rms-connector.md#installing-the-rms-connector)

-   **2단계:** [자격 증명 입력](install-configure-rms-connector.md#entering-credentials)

-   **3단계:** [RMS 커넥터를 사용하도록 서버에 권한 부여](install-configure-rms-connector.md#authorizing-servers-to-use-the-rms-connector)

-   **4단계:** [부하 분산 및 고가용성 구성](install-configure-rms-connector.md#configuring-load-balancing-and-high-availability)

-   선택 사항: [HTTPS를 사용하도록 RMS 커넥터 구성](install-configure-rms-connector.md#configuring-the-rms-connector-to-use-https)

-   선택 사항: [웹 프록시 서버에 대해 RMS 커넥터 구성](install-configure-rms-connector.md#configuring-the-rms-connector-for-a-web-proxy-server)

-   선택 사항: [관리 컴퓨터에 RMS 커넥터 관리 도구 설치](install-configure-rms-connector.md#installing-the-rms-connector-administration-tool-on-administrative-computers)

-   **5단계:** [RMS 커넥터를 사용하도록 서버 구성](configure-servers-rms-connector.md)

    -   [커넥터를 사용하도록 Exchange Server 구성](configure-servers-rms-connector.md#configuring-an-exchange-server-to-use-the-connector)

    -   [커넥터를 사용하도록 SharePoint Server 구성](configure-servers-rms-connector.md#configuring-a-sharepoint-server-to-use-the-connector)

    -   [커넥터를 사용하도록 파일 분류 인프라용 파일 서버 구성](configure-servers-rms-connector.md#configuring-a-file-server-for-file-classification-infrastructure-to-use-the-connector)


## RMS 커넥터의 사전 요구 사항
RMS 커넥터를 설치하기 전에 먼저 다음 요구 사항이 설정되어 있는지 확인하세요.

|요구 사항|추가 정보|
|---------------|--------------------|
|권한 관리(RMS) 서비스가 활성화됨|[Azure 권한 관리 활성화](activate-service.md)|
|온-프레미스 Active Directory 포리스트와 Azure Active Directory 간 디렉터리 동기화|RMS를 활성화한 후 Active Directory 데이터베이스의 사용자 및 그룹과 작동하도록 Azure Active Directory를 구성해야 합니다.<br /><br />**중요**: 테스트 네트워크인 경우에도 RMS 커넥터가 작동하려면 이 디렉터리 동기화 단계를 수행해야 합니다. 수동으로 Azure Active Directory에서 만든 계정으로 Office 365 및 Azure Active Directory를 사용할 수 있기는 하지만 이 커넥터를 사용하려면 Azure Active Directory의 계정을 Active Directory 도메인 서비스와 동기화해야 합니다. 수동 암호 동기화로는 부족합니다.<br /><br />자세한 내용은 다음 리소스를 참조하세요.<br /><br />[Azure AD 테넌트 구성 지침](http://technet.microsoft.com/library/hh967611.aspx)<br /><br />[DirSync를 통한 디렉터리 동기화 사용 지침](http://technet.microsoft.com/library/hh967642.aspx)|
|선택 사항이지만 권장 사항임:<br /><br />온-프레미스 Active Directory와 Azure Active Directory 간에 페더레이션 사용|온-프레미스 디렉터리와 Azure Active Directory 간에 ID 페더레이션을 사용하도록 설정할 수 있습니다. 이 구성을 통해 RMS 서비스에 Single Sign-On을 사용하여 더 원활한 사용자 환경이 가능합니다. Single Sign-On이 없으면 자격 증명을 입력해야 권한으로 보호된 콘텐츠를 사용할 수 있습니다.<br /><br />AD FS(Active Directory Federation Services)를 사용하여 Active Directory 도메인 서비스와 Azure Active Directory 간에 페더레이션을 구성하는 지침은 Windows Server 라이브러리에서 [검사 목록: AD FS를 사용하여 Single Sign-On 구현 및 관리](http://technet.microsoft.com/library/jj205462.aspx)를 참조하세요.|
|RMS 커넥터를 설치할 최소 두 대의 컴퓨터:<br /><br />다음 운영 체제 중 하나를 실행하는 64비트 물리적 컴퓨터 또는 가상 컴퓨터: Windows Server 2012 R2, Windows Server 2012 또는 Windows Server 2008 R2<br /><br />1GB 이상의 RAM<br /><br />최소 64GB의 디스크 공간<br /><br />하나 이상의 네트워크 인터페이스<br /><br />인증이 불필요한 방화벽(또는 웹 프록시)을 통한 인터넷 액세스<br /><br />RMS 커넥터와 함께 사용할 Exchange 또는 SharePoint Server 설치가 포함된 조직에서 다른 포리스트를 트러스트하는 포리스트 또는 도메인에 있어야 함|내결함성 및 고가용성을 위해 최소 두 대의 컴퓨터에 RMS 커넥터를 설치해야 합니다.<br /><br />**팁**: Outlook Web Access를 사용하거나 Exchange ActiveSync IRM을 사용하는 모바일 장치를 사용하고 있으며 Azure RMS로 보호되는 메일 및 첨부 파일에 대한 액세스를 유지 관리해야 하는 경우에는 부하 분산된 커넥터 서버 그룹을 배포하여 높은 가용성을 보장하는 것이 좋습니다.<br /><br />커넥터를 실행하기 위한 전용 서버는 불필요하지만, 커넥터를 사용할 서버가 아닌 별도의 컴퓨터에 커넥터를 설치해야 합니다.<br /><br />**중요**: Azure RMS에 Exchange Server, SharePoint Server 또는 파일 분류 인프라에 대해 구성된 파일 서버의 기능을 사용하려면 이러한 서비스를 실행하는 컴퓨터에 커넥터를 설치하지 마세요. 또한 도메인 컨트롤러에 이 커넥터를 설치하지 마세요.|

## 다음 단계

[Azure 권한 관리 커넥터 설치 및 구성](install-configure-rms-connector.md)으로 이동합니다.

<!--HONumber=Apr16_HO3-->

