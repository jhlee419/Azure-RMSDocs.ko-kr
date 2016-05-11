---
# required metadata

title: 시나리오 - 가장 중요한(소수) 파일 보호 | Azure RMS
description:
keywords:
author: cabailey
manager: mbaldwin
ms.date: 04/28/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: 95f1844a-612c-4e67-bbe6-4b6b92295221

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: esaggese
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# 시나리오 - 가장 중요한(소수) 파일 보호
이 시나리오와 지원 사용자 문서에서는 Azure 권한 관리를 통해 가장 중요한 파일로 식별된 소수의 파일을 수동으로 사용자 지정 보호하여 무단 액세스로부터 가장 높은 수준의 보호를 제공합니다. 일반적으로 소수의 사용자만 액세스할 수 있어야 하는 파일입니다. 예를 들어 회사의 대표 식료품에 대한 조리법 지침이나 지정된 날짜 전에 공개되면 안 되는 인수 계획입니다.

지침을 제공하기에 적합한 상황은 다음과 같습니다.

-   보호할 작은 파일 집합을 식별한 경우

-   파일이 Rights Management를 지원하는 Office 파일 형식 중 하나인 경우. 파일이 다른 파일 형식(예: CAD 파일)인 경우 이러한 형식이 Azure RMS를 지원해야 하며, 기본적으로 Azure RMS를 지원하는 응용 프로그램을 배포해야 합니다. 자세한 내용은 [응용 프로그램이 Azure 권한 관리를 지원하는 방식](https://technet.microsoft.com/library/jj585004.aspx)을 참조하세요.

-   파일에 소수의 사용자만 액세스할 수 있어야 하는 중요한 기밀 정보가 들어 있는 경우.

-   파일에 액세스할 때마다 권한을 부여하기 위해 인터넷 연결이 필요하지만 보다 높은 수준의 보안을 제공하기 때문에 이러한 불편은 감수할 수 있습니다.

-   해당 사용자에게는 이 정보를 다른 사용자와 공유해야 하는 요구 사항이 없지만 정보를 수정하고 변경 내용을 저장할 수 있습니다.

-   관리자가 파일에 액세스할 수 있는 사용자와 시기를 추적하고 필요한 경우 액세스 권한을 취소할 수 있어야 하는 경우

## 배포 지침
![](../media/AzRMS_AdminBanner.png)

사용자 문서를 진행하기 전에 다음 요구 사항이 충족되었는지 확인한 다음 지원 절차에 대한 지침을 따르세요.

## 이 시나리오의 요구 사항
이 시나리오의 경우 다음 사항을 준비해야 합니다.

|요구 사항|추가 정보가 필요한 경우 확인 가능한 위치|
|---------------|--------------------------------|
|Office 365 또는 Azure Active Directory용 계정과 그룹을 준비했는지 여부<br /><br />기밀 문서에 액세스할 수 있어야 하는 소수의 사용자를 포함하는 **Privileged access**라는 메일 사용이 가능한 그룹<br /><br />작업에 eDiscovery, 모니터링 및 감사가 포함된 사용자를 포함하는 **IT Compliance managers**라는 메일 사용이 가능한 그룹<br /><br />**RMS administrators**라는 메일 사용이 가능한 그룹이 있고 Azure RMS를 구성하는 모든 관리자가 이 그룹의 구성원인지 여부|[Azure 권한 관리 준비](https://technet.microsoft.com/library/jj585029.aspx)|
|Azure 권한 관리가 활성화되었는지 여부|[Azure 권한 관리 활성화](https://technet.microsoft.com/library/jj658941.aspx)|
|다음에 설명하는 대로 사용자 지정 템플릿을 구성했는지 여부|[Azure 권한 관리용 사용자 지정 템플릿 구성](https://technet.microsoft.com/library/dn642472.aspx)|
|다음 섹션에 설명된 대로 이러한 파일을 바로 보호할 수 있도록 Rights Management 공유 응용 프로그램이 사용자의 Windows 컴퓨터에 배포되었는지 여부|[Rights Management 공유 응용 프로그램 다운로드 및 설치 ](https://technet.microsoft.com/library/dn574734%28v=ws.10%29.aspx)|
|권한 있는 사용자에게 최소 Office 2013 이상의 버전이 있는지 여부|사용자에게 Office 2010이 있는 경우 Rights Management 공유 응용 프로그램도 설치해야 합니다.|
|Azure RMS 구독에 문서 추적이 포함되는지 여부|Azure RMS 구독에 문서 추적 및 취소 기능이 포함되어 있지 않으면 문서 추적 사이트를 사용하여 이러한 문서에 액세스하는 사용자를 확인하고 필요한 경우 액세스 권한을 취소할 수 없습니다. 이 경우 문서 추적 기능을 지원하는 구독을 구입하거나 이러한 제한을 감수합니다. 또한 Azure RMS의 [사용 현황 로깅](https://technet.microsoft.com/library/dn529121.aspx) 기능을 사용하는 것이 좋습니다. 이 기능은 각 파일에 액세스한 사용자와 시기 등의 정보를 제공하므로 잠재적으로 의심스러운 행동을 검색하는 데 도움이 됩니다.<br /><br />구독 지원을 확인하려면 [RMS(Rights Management Services) 제품 비교](https://technet.microsoft.com/dn858608)를 참조하세요.|

### 사용자 지정 템플릿을 구성하려면

1.  Azure 클래식 포털에서 다음 값과 설정이 포함된 Azure 권한 관리용 사용자 지정 템플릿을 새로 만듭니다.

    -   이름: **Privileged access**

    -   권한: 메일 사용이 가능한 **Privileged access** 그룹에 **공동 소유자** 권한 부여

    -   범위: 메일 사용이 가능한 **Privileged access** 그룹, 메일 사용이 가능한 **IT Compliance managers** 그룹 및 메일 사용이 가능한 **RMS administrators** 그룹을 선택합니다.

    -   오프라인 액세스: **콘텐츠는 인터넷이 연결된 동안에만 사용할 수 있습니다.**

2.  새 템플릿을 게시합니다.

### 파일을 바로 보호하려면

1.  파일 탐색기에서 보호할 파일이 포함된 첫 번째 폴더로 이동합니다.

    -   폴더에 있는 모든 파일을 보호하려면 폴더를 선택합니다.

    -   폴더에 있는 일부 파일만 보호하려면 보호할 폴더를 다중 선택합니다.

2.  마우스 오른쪽 단추를 클릭하고 **RMS로 보호**를 선택한 다음 **바로 보호**를 선택합니다.

3.  **Privileged access**를 선택합니다.

4.  자격 증명을 입력하라는 메시지가 표시될 수 있습니다. 파일이 보호될 때까지 기다린 후 **파일이 보호되었습니다.** 페이지가 표시되면 **닫기**를 클릭합니다.

5.  다른 폴더에 보호할 파일이 더 있는 경우 각 폴더에 대해 1-4단계를 반복합니다.

파일을 바로 보호하는 방법에 대한 자세한 내용은 [Rights Management 공유 응용 프로그램을 사용하여 장치에서 파일 보호(바로 보호)](https://technet.microsoft.com/library/dn574733%28v=ws.10%29.aspx)를 참조하세요.

> [!TIP]
> 이 수동 프로세스에서 보호할 파일 수가 너무 많은 경우 [RMS 보호 도구](https://www.microsoft.com/en-us/download/details.aspx?id=47256)를 사용하여 템플릿을 통해 파일을 대량 보호하는 것이 좋습니다.

### 파일 액세스를 모니터링하고 필요한 경우 액세스 권한을 취소하려면

1.  파일 탐색기에서 보호된 파일을 마우스 오른쪽 단추로 클릭하고 **RMS로 보호**를 선택한 다음 **사용 현황 추적**을 선택합니다.

2.  메시지가 표시되면 로그인하여 문서 추적 사이트에 액세스합니다.

3.  파일 및 보호한 다른 파일에 액세스한 사용자를 확인하고 의심스러운 행동을 나타내는 경우 실패한 시도에 특히 주의합니다. 타당한 경우 각 파일에 대한 액세스 권한을 취소할 수 있습니다.

## 사용자 문서 지침
이러한 파일에는 사용자의 특별한 작업이 필요하지 않기 때문에 이 시나리오의 경우 사용자에게 제공할 특정 지침이 없습니다. 직접 파일을 보호했으며 모니터링합니다. 그러나 어떤 파일이 보호되었으며 이로 인해 문서 사용이 어떻게 제한될 수 있는지를 사용자와 지원 채널에 알려야 할 수도 있습니다. 예를 들어 권한 있는 사용자라도 인터넷 연결이 없을 경우 파일을 열 수 없습니다.

다음 템플릿을 사용하여 최종 사용자 통신에 알림을 복사해서 붙여넣고 다음과 같이 수정합니다.

1.  파일의 실제 이름을 제공하거나 권한 있는 사용자가 이해하는 명확한 참조를 사용합니다.

2.  &lt;연락처 세부 정보&gt;를 해당 사용자가 문서의 중요도와 일치하는 에스컬레이션된 지원 채널을 통해 지원 센터나 IT 부서에 연락할 수 있는 방법에 대한 지침으로 바꿉니다. 예를 들어 심각도가 높은 지원 통화에는 24시간 전화 번호를 제공합니다.

3.  알림을 원하는 대로 수정한 다음 해당 사용자에게 보냅니다.

예제 문서에서는 사용자 지정 후 이 알림이 사용자에게 표시되는 방식을 보여 줍니다.

![](../media/AzRMS_UsersBanner.png)

### IT 알림: &lt;조직 이름&gt;의 기밀 문서 보호
다음 파일은 &lt;제한된 사용자&gt;만 파일에 액세스하고 변경할 수 있도록 매우 높은 수준의 보호가 적용되어 있습니다. 무단 액세스로부터 파일을 보호하기 위해 파일을 열 때마다 응용 프로그램에서 자동으로 권한 부여를 요청하므로 이제 파일을 열려면 인터넷 연결이 있어야 하며 자격 증명을 묻는 메시지가 표시될 수도 있습니다.

-   &lt;기밀 문서, 형식 또는 위치 1&gt;

-   &lt;기밀 문서, 형식 또는 위치 2&gt;

-   &lt;기밀 문서, 형식 또는 위치 3&gt;

**도움이 필요하십니까?**

-   이러한 파일에 액세스할 수 없거나 파일에서 의심스러운 변경 내용을 발견하는 경우 &lt;작업 및 연락처 세부 정보&gt;.

#### 예제 사용자 지정 사용자 문서
![](../media/AzRMS_ExampleBanner.png)

##### IT 알림: VanArsdel의 기밀 문서 보호
다음 파일은 이 메일 메시지의 받는 사람 줄에 있는 사용자만 파일에 액세스하고 변경할 수 있도록 매우 높은 수준의 보호가 적용되어 있습니다. 무단 액세스로부터 파일을 보호하기 위해 파일을 열 때마다 응용 프로그램에서 자동으로 권한 부여를 요청하므로 이제 파일을 열려면 인터넷 연결이 있어야 하며 자격 증명을 묻는 메시지가 표시될 수도 있습니다.

-   코드 이름 "Mercury"에 대한 디자인 사양

-   코드 이름 "Jupiter"에 대한 디자인 사양

-   코드 이름 "Saturn"에 대한 디자인 사양

-   코드 이름 "Neptune"에 대한 디자인 사양

**도움이 필요하십니까?**

-   이러한 파일에 액세스할 수 없거나 파일에서 의심스러운 변경을 발견하는 경우 IT 부서로부터 보호된 메일 메시지로 받은 24시간 지원 에스컬레이션 회선으로 전화하세요.



<!--HONumber=Apr16_HO4-->

