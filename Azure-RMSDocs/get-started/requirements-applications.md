---
# required metadata

title: Azure RMS 요구 사항&#58; 응용 프로그램 | Azure RMS
description:
keywords:
author: cabailey
manager: mbaldwin
ms.date: 04/28/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: 7b33bcb8-63da-46be-ad56-b06de97822fa

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: esaggese
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---


# Azure RMS 요구 사항: 응용 프로그램

다음 표를 사용하여 Azure RMS를 기본적으로 지원하는 응용 프로그램을 확인할 수 있습니다. 즉, 이러한 응용 프로그램에는 사용 제한을 지원하기 위해 RMS API를 통해 RMS가 긴밀하게 통합되어 있습니다. 이러한 응용 프로그램을 RMS 지원이라고도 합니다.

별도의 설명이 없으면 지원되는 기능은 Azure RMS와 AD RMS 둘 다에 적용됩니다. 또한 iOS, Android, OS X 및 Windows Phone 8.1에서 AD RMS를 지원하려면 [Active Directory Rights Management Services 모바일 장치 확장](https://technet.microsoft.com/library/dn673574.aspx)이 필요합니다.

테이블 열에 대한 정보:

-   **보호된 PDF**: 파일 이름 확장명이 .ppdf이고 RMS 공유 응용 프로그램을 사용하여 Office 파일 및 PDF 파일을 메일로 공유할 때 자동으로 생성되는 파일입니다. RMS 공유 응용 프로그램에는 보호 PDF 파일용 뷰어가 포함되어 있습니다. 이전에 Azure RMS 또는 AD RMS를 사용하여 보호된 PDF 파일을 만든 경우 Foxit Reader 및 Nitro Pro를 사용하여 Windows, iOS 및 Android 장치에서 해당 파일을 계속 읽을 수 있습니다.

-   **메일:** 나열된 메일 클라이언트는 메일 메시지 자체를 보호할 수 있으므로 첨부된 파일도 자동으로 보호됩니다. 이 시나리오에서 클라이언트의 미리 보기 기능은 권한 있는 받는 사람에게 보호된 콘텐츠(메시지 및 첨부 파일)를 표시할 수 있습니다. 그러나 전자 메일 메시지 자체가 보호되지 않고 첨부 파일만 보호되면, 클라이언트의 미리 보기 기능이 권한 있는 받는 사람에게 보호된 첨부 파일을 표시할 수 없습니다.

-   **기타 파일 형식**: 텍스트 및 이미지 파일에는 파일 이름 확장명이 .txt, .xml, .jpg, .jpeg와 같은 파일이 포함됩니다. 이러한 파일은 RMS의 기본 보호를 통해 읽기 전용으로 바뀌면 파일 확장명이 변경됩니다. 기본 보호를 적용할 수 없는 파일은 RMS의 일반적인 보호를 받으며 파일 확장명으로 .pfile이 지정됩니다. 자세한 내용은 [Rights Management 공유 응용 프로그램 관리자 가이드](../rms-client/sharing-app-admin-guide.md)를 참조하세요.


|**장치 운영 체제**|Word, Excel, PowerPoint|보호된 PDF|전자 메일|다른 파일 형식|
|-------------------------------|---------------------------|-----------------|---------|--------------------|
|**Windows**|Office 2010<br /><br />Office 2013<br /><br />Office Mobile 앱(Azure RMS에만 해당) [[1]](#footnote-1)<br /><br />Office Online [[2]](#footnote-2)|Gaaiho 문서<br /><br />GigaTrust Desktop PDF Client for Adobe<br /><br />Foxit Reader<br /><br />Nitro PDF Reader<br /><br />RMS 공유 앱 |Outlook 2010<br /><br />Outlook 2013<br /><br />OWA(Outlook Web App) [[3]](#footnote-3)<br /><br />Windows Mail [[4]](#footnote-4)|Windows용 RMS 공유 응용 프로그램: 텍스트, 이미지, pfile<br /><br />Siemens JT2Go: JT 파일(Windows 10에만 해당)|
|**iOS**|iPad 및 iPhone용 Office [[5]](#footnote-5)<br /><br />Office Online [[2]](#footnote-2)<br /><br />TITUS Docs|Foxit Reader<br /><br />RMS 공유 앱 [[1]](#footnote-1)<br /><br />TITUS Docs|Citrix WorxMail<br /><br />NitroDesk [[4]](#footnote-4)<br /><br />iPad 및 iPhone용 Outlook [[4]](#footnote-4)<br /><br />iOS용 OWA [[3]](#footnote-3)<br /><br />TITUS Mail|RMS 공유 앱 [[1]](#footnote-1): 텍스트, 이미지, pfile<br /><br />TITUS Docs: Pfile|
|**Android**|GigaTrust App for Android<br /><br />Office Online [[2]](#footnote-2)|GigaTrust App for Android<br /><br />Foxit Reader<br /><br />RMS 공유 앱 [[1]](#footnote-1)|9Folders [[4]](#footnote-4)<br /><br />GigaTrust App for Android [[4]](#footnote-4)<br /><br />Citrix WorxMail<br /><br />NitroDesk [[4]](#footnote-4)<br /><br />Android용 OWA [[3]](#footnote-3) 및 [[6]](#footnote-6)<br /><br />Samsung Email(S3 이상) [[6]](#footnote-6)<br /><br />TITUS Classification for Mobile|RMS 공유 앱 [[1]](#footnote-1): 텍스트, 이미지, pfile|
|**OS X**|Office 2011(AD RMS만 해당)<br /><br />Mac용 Office 2016<br /><br />Office Online [[2]](#footnote-2)|Foxit Reader<br /><br />RMS 공유 앱 [[1]](#footnote-1)|Outlook 2011(AD RMS만 해당)<br /><br />Mac용 Outlook 2016<br /><br />Outlook for Mac|RMS 공유 앱 [[1]](#footnote-1): 텍스트, 이미지, pfile|
|**Windows 10 Mobile**|Office Mobile 앱(Azure RMS에만 해당) [[1]](#footnote-1)|지원되지 않음|Citrix WorxMail<br /><br />Outlook 메일|지원되지 않음|
|**Windows RT**|Office 2013 RT<br /><br />Office Online [[2]](#footnote-2)|지원되지 않음|Outlook 2013 RT<br /><br />Windows용 메일 앱<br /><br />Windows Mail [[4]](#footnote-4)|Siemens JT2Go: JT 파일|
|**Windows Phone 8.1**|Office Mobile(AD RMS만 해당)|RMS 공유 앱 [[1]](#footnote-1)|Outlook Mobile [[4]](#footnote-4)|RMS 공유 앱 [[1]](#footnote-1): 텍스트, 이미지, pfile|
|**Blackberry 10**|지원되지 않음|지원되지 않음|Blackberry 메일 [[4]](#footnote-4)|지원되지 않음|


###### 각주 1
사용권 계약에 따라 보호하는 콘텐츠 보기를 지원합니다.

###### 각주 2 
SharePoint Online, 비즈니스용 OneDrive, Outlook Web Access에서 사용권 계약에 따라 보호하는 콘텐츠 보기를 지원합니다.

###### 각주 3
Exchange 온-프레미스에 사서함이 있는 받는 사람이 보호된 메일을 수신하는 경우 이 콘텐츠는 Outlook과 같은 서식 있는 메일 클라이언트에서만 열 수 있습니다.  이 콘텐츠는 Outlook Web Access에서 열 수 없습니다.

###### 각주 4
Exchange 관리자가 사용하도록 설정해야 하는 Exchange ActiveSync IRM을 사용합니다. 사용자는 보호된 전자 메일 메시지를 보기, 회신 및 전체 회신할 수 있지만 사용자는 새 전자 메일 메시지 자체를 보호할 수 없습니다.

Exchange 온-프레미스에 사서함이 있는 받는 사람이 Exchange를 사용하는 다른 조직으로부터 보호된 전자 메일을 수신하는 경우 이 콘텐츠는 Outlook과 같은 서식 있는 전자 메일 클라이언트에서만 열 수 있습니다.  이 콘텐츠는 Exchange Active Sync IRM을 사용하는 장치에서 열 수 없습니다.

###### 각주 5
보호된 문서 보기 및 편집을 지원합니다. 자세한 내용은 Office 블로그에서 [iPad 및 iPhone용 Office에 Azure 권한 관리 지원 제공](https://blogs.office.com/2015/07/22/azure-rights-management-support-comes-to-office-for-ipad-and-iphone-2/) 게시물을 참조하세요.

###### 각주 6
자세한 내용은 Office 블로그에서 [이제 일부 선택된 장치에서 Android용 OWA를 사용할 수 있음](http://blogs.office.com/2014/06/11/owa-for-android-now-available-on-select-devices/) 게시물을 참조하세요.

## Office에 대한 Azure RMS 지원과 관련된 자세한 내용

Office 2007을 제외하고 모든 버전의 Office에서 보호된 콘텐츠를 사용할 수 있습니다.

Office Professional Plus 2010 또는 Office Professional 2010을 사용하는 Azure RMS:

- Windows용 Rights Management 공유 응용 프로그램이 필요

- Windows 10에서는 지원되지 않음


## Rights Management 공유 응용 프로그램에 대한 자세한 내용

Windows용 Rights Management 공유 응용 프로그램에 대한 자세한 내용은 다음 리소스를 참조하세요.

-   [Rights Management 공유 응용 프로그램 관리자 가이드](../rms-client/sharing-app-admin-guide.md)

-   [Rights Management 공유 응용 프로그램 사용자 가이드](../rms-client/sharing-app-user-guide.md)

모바일 플랫폼용 Rights Management 공유 응용 프로그램에 대한 자세한 내용은 다음 리소스를 참조하세요.

-   [Microsoft Rights Management 페이지](http://go.microsoft.com/fwlink/?LinkId=303970)의 링크를 사용하여 관련 앱 다운로드

-   Microsoft Intune이 있는 경우 정책 관리된 앱을 사용하여 앱을 배포하고 관리할 수 있습니다. 

    -   Intune에서 등록된 iOS 및 Android 장치의 경우: [Microsoft Intune 콘솔에서 모바일 응용 프로그램 관리 정책 구성 및 배포](/intune/deploy-use/configure-and-deploy-mobile-application-management-policies-in-the-microsoft-intune-console)

    -   Intune에서 등록되지 않은 Android 장치의 경우: [Microsoft Intune으로 모바일 앱 관리 정책 만들기 및 배포](/intune/deploy-use/create-and-deploy-mobile-app-management-policies-with-microsoft-intune)

-   [모바일 플랫폼용 Microsoft Rights Management 공유 응용 프로그램 FAQ](https://technet.microsoft.com/dn451248)



## Azure RMS를 지원하는 다른 응용 프로그램에 대한 자세한 내용

표에 있는 응용 프로그램뿐 아니라 RMS API를 Azure RMS와 통합할 수 있도록 지원하는 모든 응용 프로그램이며, 다음이 포함됩니다.

- RMS SDK를 사용하여 사내에서 작성한 LOB(기간 업무) 응용 프로그램

- 소프트웨어 공급업체에서 RMS SDK를 사용하여 작성한 응용 프로그램

SDK에 대한 자세한 내용은 [Microsoft Rights Management SDK](../develop/developers-guide.md)를 참조하세요.

## Azure RMS에서 지원되지 않는 응용 프로그램

Azure RMS에서 현재 지원되지 않는 응용 프로그램은 다음과 같습니다.

-   Microsoft Office for Mac 2011

-   SharePoint Server 2013에 대한 Microsoft 비즈니스용 OneDrive

-   XPS 뷰어
 
또한 RMS 공유 응용 프로그램에는 다음과 같은 제한이 있습니다.

-   Windows 컴퓨터의 경우: 최소 Windows 7 서비스 팩 1 이상 버전이 필요합니다.



## 다음 단계
기타 요구 사항을 확인하려면 [Azure 권한 관리 요구 사항](requirements-azure-rms.md)을 참조하세요.

자주 사용하는 응용 프로그램이 Azure RMS를 지원하는 방식에 대한 자세한 내용은 [응용 프로그램이 Azure 권한 관리를 지원하는 방식](../understand-explore/applications-support.md)을 참조하세요.

자주 사용하는 응용 프로그램을 Azure RMS에 대해 구성하는 방법에 대한 자세한 내용은 [Azure 권한 관리에 대해 응용 프로그램 구성](../deploy-use/configure-applications.md)을 참조하세요.

<!--HONumber=Apr16_HO4-->

