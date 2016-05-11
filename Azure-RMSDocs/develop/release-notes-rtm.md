---
# required metadata

title: 릴리스 정보 | Azure RMS
description:
keywords:
author: bruceperlerms
manager: mbaldwin
ms.date: 04/28/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: 84a93d5b-37e9-4d9c-9b7c-ad00963a68d7

# optional metadata

#ROBOTS:
audience: developer
#ms.devlang:
ms.reviewer: shubhamp
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

﻿
# 릴리스 정보

이 항목에는 이 릴리스와 이전 릴리스의 RMS SDK 2.1에 대한 중요한 정보가 포함되어 있습니다.

## 2015년 12월 업데이트의 새로운 기능

-   다음을 포함하여 여러 영역에서 성능 향상이 구현되었습니다.

    라이선스 전용 서버를 사용하는 경우 기본 라이선스 서버에서 게시합니다.

    네트워크 연결이 없는 경우 RMS SDK 2.1이 더 빨리 실패합니다.

-   오류 메시지 및 문제 해결 환경을 개선하기 위한 많은 업데이트.
-   [지원되는 플랫폼](supported-platforms.md) 목록도 업데이트되었습니다.

## 2015년 5월 업데이트

-   **서비스 앱 및 클라우드 기반 RMS** - [**IPC\_CREDENTIAL\_SYMMETRIC\_KEY**](/rights-management/sdk/2.1/api/win/ipc_credential#msipc_ipc_credential_symmetric_key)에는 대칭 키, **AppPrincipalId** 및 **TenantBposId**의 세 가지 정보가 필요합니다. 이와 관련된 항목이 획득한 이 정보의 처리 지침을 제공하도록 업데이트되었습니다. 이 업데이트에 대해서는 [서비스 응용 프로그램이 클라우드 기반 RMS를 사용할 수 있도록 설정](how-to-use-file-api-with-aadrm-cloud.md)의 업데이트된 버전을 참조하세요.

## 2015년 4월 업데이트

-   이제 새로운 API 집합을 통해 **문서 추적**을 사용할 수 있습니다. 자세한 내용은 [콘텐츠 추적](tracking-content.md)을 참조하세요.
-   **암호화 유형** - 이제 암호화 패키지 선택에 대해 API 수준 제어를 지원합니다. 자세한 내용은 [암호화 작업](working-with-encryption.md)을 참조하세요.

    **참고** **IPC\_LI\_DEPRECATED\_ENCRYPTION\_ALGORITHMS** 플래그는 더 이상 API에 노출되지 않습니다. 즉, 이후 앱에서 이 플래그를 참조할 경우 더 이상 컴파일되지 않지만 API 코드에서 비공개로 플래그가 적용되므로 이미 빌드된 앱은 계속 작동합니다. 플래그를 변경하기만 하면 사용되지 않는 이전 암호화 알고리즘 플래그를 여전히 활용할 수 있습니다. 자세한 내용은 [암호화 작업](working-with-encryption.md)을 참조하세요.

     

-   [**API 모드 값**](/rights-management/sdk/2.1/api/win/api%20mode%20values#msipc_api_mode_values_IPC_API_MODE_SERVER)이 **IPC\_API\_MODE\_SERVER**인 **서버 모드 응용 프로그램**에는 응용 프로그램 매니페스트가 더 이상 필요하지 않습니다. 프로덕션 RMS 서버에서 응용 프로그램을 테스트할 수 있으며, 프로덕션 환경으로 전환할 때 프로덕션 라이선스를 얻지 않아도 됩니다. 서버 모드 응용 프로그램에 대한 자세한 내용은 [응용 프로그램 종류](application-types.md)를 참조하세요.
-   이제 **로깅**이 파일 및 Windows용 이벤트 추적 방법 둘 다를 통해 구현됩니다.
-   **Windows 7 SP1 또는 Windows Server 2008 R2 컴퓨터**에서 실행하는 경우 "중요한 개발자 노트" 아래에 있는 참고 사항을 참조하세요.

## 2015년 1월 업데이트

-   **지원되는 보호된 파일(pfile) 크기 증가** - 이제 1GB보다 큰 pfile 크기를 지원합니다. pfile에 대한 자세한 내용은 [지원 파일 형식](supported-file-formats.md)을 참조하세요.
-   **더 나은 진단을 위한 향상된 로깅** - 로깅 수준에서 검토해야 하는 메시지에 대해 **오류** 또는 **경고**가 표시됩니다. 여전히 표시되는 예외를 포함하여 다른 모든 메시지는 **정보**로 기록됩니다.

    세부 정보가 손실되지 않도록 이 방법을 선택했습니다. 이제 중요한 메시지만 경고 수준으로 표시됩니다.

-   **회사 템플릿 가져오기** – 고객 보고서 및 피드백에 따라 템플릿 가져오기 코드가 상당히 수정되었습니다.
-   향상된 지역화 일관성

## 2014년 10월 업데이트

-   SDK의 파일 API 구성 요소에 대한 기본 동작이 업데이트되었습니다. 자세한 내용은 [파일 API 구성](file-api-configuration.md)을 참조하세요.
-   새로운 기능인 메일 알림은 개발자 노트 항목인 [메일 알림 사용](how-to-enable-email-notification.md)에서 설명합니다.

## 2014년 7월 업데이트

SDK의 파일 API 구성 요소가 확장되었으며 다음 기능을 제공합니다.

-   사용할 보호기를 식별합니다.
-   파일 세분성 수준에서 RMS 보호 기능을 제공합니다.

    이 릴리스에서 추가된 함수:

    **참고** 여기에 나열되지 않은 추가 지원 데이터 형식 및 구조체가 파일 API 확장을 위해 추가되었습니다. 이 릴리스에서 업데이트된 모든 항목에는 **임시 및 변경될 수 있음**이 표시됩니다.

     

    -   [**IpcfOpenFileOnHandle**]()
    -   [**IpcfOpenFileOnILockBytes**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcfopenfileonilockbytes)
    -   [**IpcfGetFileProperty**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcfgetfileproperty)
    -   [**IpcfLogicalFileRangeToRawFileRange**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcflogicalfilerangetorawfilerange)
    -   [**IpcfReadFile**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcfreadfile)
    -   [**IpcfSetEndOfFile**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcfsetendoffile)
    -   [**IpcfWriteFile**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcfwritefile)

## 2014년 4월 업데이트

-   특히 큰 PFile의 경우 **파일 API 메모리 사용**이 훨씬 향상되었습니다.
-   이제 **IPC\_LI\_CONTENT\_ID** 속성을 통해 **콘텐츠 ID**를 쓸 수 있습니다. 자세한 내용은 [**라이선스 속성 형식**](/rights-management/sdk/2.1/api/win/License%20property%20types#msipc_license_property_types_IPC_LI_APP_SPECIFIC_DATA)을 참조하세요.
-   **프로덕션 매니페스트 요구 사항** - 서버 모드에서 RMS 사용 응용 프로그램/서비스를 실행하는 경우에는 더 이상 매니페스트가 필요하지 않습니다. 자세한 내용은 [응용 프로그램 종류](application-types.md)를 참조하세요.
-   **설명서 업데이트**

    **재구성됨** - 환경 설정 및 응용 프로그램 테스트 단계 순서를 명확하게 설명하기 위해 [사용 방법](how-to-use-msipc.md)이 재구성되었습니다.

    **테스트 모범 사례** - Azure RMS를 사용하여 테스트하기 전에 온-프레미스 서버를 사용하는 지침이 추가되었습니다. 자세한 내용은 [서비스 응용 프로그램이 클라우드 기반 RMS를 사용할 수 있도록 설정](how-to-use-file-api-with-aadrm-cloud.md)을 참조하세요.

## 중요한 개발자 노트

-   **모든 파일 형식에 대한 기본 지원**

    이 릴리스의 권한 관리 서비스 SDK 2.1에서는 모든 파일 형식(확장명)에 대해 기본 지원을 추가할 수 있습니다. 예를 들어 &lt;ext&gt; 확장명(비 Office 및 pdf)의 경우 해당 확장명에 대한 관리자 구성이 "NATIVE"이면 \*.p&lt;ext&gt;가 사용됩니다.

    지원되는 파일 형식에 대한 자세한 내용은 [파일 API 구성](file-api-configuration.md)을 참조하세요.

-   [KB2533623](https://support.microsoft.com/en-us/kb/2533623) 업데이트가 없는 **Windows 7 SP1 및 Windows Server 2008 R2 SP1 컴퓨터**에서는 Office 파일을 보호하는 중 "매개 변수가 잘못되었습니다. 오류 코드 0x80070057"이라는 오류가 발생할 수 있습니다. 이 오류가 표시되면 업데이트를 설치하고 다시 시도하세요. 그래도 문제가 표시되면 RMS SDK 베타 피드백 별칭인 <rmcstbeta@microsoft.com>으로 문의하세요.

    **참고** 2015년 4월 릴리스를 기준으로, 이 기술 자료에 대한 확인이 설치 프로세스에 추가되었습니다.

     

-   **파일 API 통합**

    파일 API가 추가된 Active Directory Rights Management Services 파일 API는 다음과 같은 혜택과 기능을 제공합니다.

    다양한 파일 형식에서 사용되는 IRM(정보 권한 관리) 구현의 세부 정보를 알 필요 없이 자동화된 방식으로 기밀 데이터를 보호할 수 있습니다.

    기본 보호를 사용하여 Microsoft Office 파일, PDF(Portable Document Format) 파일 및 선택한 다른 파일 형식을 보호할 수 있습니다. 기본 보호를 사용하여 보호할 수 있는 파일 형식의 전체 목록은 [파일 API 구성](file-api-configuration.md)을 참조하세요.

    RMS 보호된 파일 형식(PFile)을 사용하여 시스템 파일 및 Office 파일을 제외한 모든 파일을 보호할 수 있습니다.

-   **문제**: 라이선스를 처음부터 만드는 경우 소유권 권한을 명시적으로 부여해야 합니다.

    **해결 방법**: [**IpcCreateLicenseFromScratch**](/rights-management/sdk/2.1/api/win/functions#msipc_ipccreatelicensefromscratch)를 사용하여 라이선스를 처음부터 만드는 경우 응용 프로그램에서 라이선스 소유자에게 **소유자** 권한을 명시적으로 추가해야 합니다. 자세한 내용은 [명시적 소유자 권한 추가](add-explicit-owner-rights.md)를 참조하세요.

-   **문제**: 응용 프로그램이 해당 핸들을 사용하여 동일한 창에 대해 [**IpcProtectWindow**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcprotectwindow) 또는 [**IpcUnprotectWindow**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcunprotectwindow)를 두 번 호출하는 경우 RMS SDK 2.1에서 **HRESULT**에 오류를 반환합니다.

    **해결 방법**: 이 문제에 대한 특정 지침은 [**IpcProtectWindow**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcprotectwindow) 및 [**IpcUnprotectWindow**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcunprotectwindow)에서 설명 섹션을 참조하세요.

-   **문제**: 여러 아키텍처에 대해 빌드하는 경우 이 지침을 따라야 합니다.

    **해결 방법**: 다른 아키텍처에서 Ipcsecproc\*isv.dll을 사용하려는 경우(예를 들어 64비트 컴퓨터에 64비트 SDK를 설치했지만 이제 Ipcsecproc\*isv.dll이 필요한 32비트 컴퓨터에 배포하려는 경우), 다른 컴퓨터에 32비트 SDK를 설치하고 "%PROGRAMFILES%\\Microsoft Information Protection And Control" 폴더(기본 위치 또는 SDK를 설치하도록 선택한 위치)에서 Ipcsecproc\*isv.dll 파일을 복사해야 합니다.

## 질문과 대답

**Q**: LCID 매개 변수를 사용하는 함수에서 기본 언어 동작이 어떻게 작동하나요?

**A**: 기본 로캘의 경우 0을 사용합니다. 이 경우 AD RMS 클라이언트 2.1은 이름과 설명을 다음 순서로 조회하고 사용 가능한 첫 번째 항목을 검색합니다.

1 - 사용자 기본 설정 LCID
2 - 시스템 로캘 LCID
3 - RMS(권한 관리 서버) 템플릿에 지정된 사용 가능한 첫 번째 언어
이름 및 설명을 검색할 수 없으면 오류가 반환됩니다. 특정 LCID마다 하나의 이름과 설명만 사용할 수 있습니다.

## 관련 항목

* [개요](ad-rms-overview.md)
* [명시적 소유자 권한 추가](add-explicit-owner-rights.md)
* [파일 API 구성](file-api-configuration.md)
* [**IpcfGetSerializedLicenseFromFile**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcfgetserializedlicensefromfile)
* [**IpcfEncryptFile**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcfencryptfile)
* [**IpcfDecryptFile**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcfdecryptfile)
* [**IpcfIsFileEncrypted**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcfisfileencrypted)
* [**IpcCreateLicenseFromScratch**](/rights-management/sdk/2.1/api/win/functions#msipc_ipccreatelicensefromscratch)
* [**IpcProtectWindow**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcprotectwindow)
* [**IpcUnprotectWindow**](/rights-management/sdk/2.1/api/win/functions#msipc_ipcunprotectwindow)
 

 





<!--HONumber=Apr16_HO3-->

