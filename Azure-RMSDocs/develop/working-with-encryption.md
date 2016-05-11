---
# required metadata

title: 암호화 작업 | Azure RMS
description:
keywords:
author: bruceperlerms
manager: mbaldwin
ms.date: 04/28/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: 088c98f9-f06e-4aae-8fac-bc7605e545f5

# optional metadata

#ROBOTS:
audience: developer
#ms.devlang:
ms.reviewer: shubhamp
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

﻿# 암호화 작업

이 항목에서는 암호화 패키지에 대해 설명하고 사용과 관련된 몇 가지 코드 조각을 보여 줍니다.

## 새 기본값, AES 256 지원

RMS SDK 2.1 2015년 3월 업데이트 이상에 대해 빌드한다고 가정할 경우 AES 256 기반 암호화가 새 기본값이기 때문에 추가 코드 없이 사용할 수 있습니다. AES 256의 보안 강화 혜택을 활용하려면 응용 프로그램을 이 릴리스로 업데이트하는 것이 좋습니다.

> [!IMPORTANT]
> AES 256 보호된 파일 사용은 [2014년 10월 릴리스](release-notes-rtm.md)부터 지원되었습니다. 2014년 10월 이전 버전의 SDK로 빌드한 응용 프로그램을 실행하는 경우 이 업데이트를 사용하면 응용 프로그램이 중단됩니다. 빌드하는 응용 프로그램의 고객이 업데이트된 SDK를 사용 중이거나 최신 버전의 응용 프로그램으로 즉시 업데이트할 의향이 있는지 확인합니다.

 
## API 암호화 지원

[2015년 3월 업데이트](release-notes-rtm.md) 이상에서는 API 및 관련된 암호화 패키지에 다음 세 가지 플래그가 통합되었습니다.

-   IPC\_ENCRYPTION\_PACKAGE\_AES256\_CBC4K
-   IPC\_ENCRYPTION\_PACKAGE \_AES128\_CBC4K
-   IPC\_ENCRYPTION\_PACKAGE \_AES128\_ECB(사용되지 않는 알고리즘이라고도 함)

암호화 패키지 플래그([**기본 암호화**](/rights-management/sdk/2.1/api/win/constants#msipc_preferred_encryption) 참조)를 새 라이선스 속성 플래그 **IPC\_LI\_PREFERRED\_ENCRYPTION\_PACKAGE**와 함께 사용할 수 있습니다.

다음은 새 라이선스 속성을 사용하는 방법을 보여 주는 몇 가지 간단한 코드 조각입니다.

## 사용되지 않는 알고리즘

**IPC\_LI\_DEPRECATED\_ENCRYPTION\_ALGORITHMS** 플래그는 더 이상 API에 노출되지 않습니다. 즉, 이후 응용 프로그램에서 이 플래그를 참조할 경우 더 이상 컴파일되지 않지만 API 코드에서 비공개로 플래그가 적용되므로 이 플래그를 사용하여 이미 빌드된 응용 프로그램은 계속 작동합니다.

플래그를 변경하기만 하면 사용되지 않는 이전 암호화 알고리즘 플래그를 여전히 활용할 수 있습니다. 예제는 다음 코드 조각을 참조하세요.

## AES 256 CBC4K를 사용하여 파일 보호

AES 256 CBC4K가 기본값이므로 코드를 변경할 필요가 없습니다.

    
    hr = IpcCreateLicenseFromTemplateID(pcTil-&gt;aTi[0].wszID, 
                                    0, 
                                    NULL, 
                                    &amp;pLicenseHandle);
    

## AES-128 CBC4K를 사용하여 파일 보호

    
    hr = IpcCreateLicenseFromTemplateID(pcTil-&gt;aTi[0].wszID, 
                                    0, 
                                    NULL, 
                                    &amp;pLicenseHandle);
    
    DWORD dwEncryptionMode = IPC_ENCRYPTION_PACKAGE_AES128_CBC4K; 
    
    hr = IpcSetLicenseProperty(pLicenseHandle, 
                           false,
                           IPC_LI_PREFERRED_ENCRYPTION_PACKAGE,
                           &amp;dwEncryptionMode);
    

## AES-128 ECB(사용되지 않는 알고리즘)를 사용하여 파일 보호

또한 이 샘플에서는 사용되지 않는 알고리즘을 지원하는 새로운 방법을 보여 줍니다.

    
    hr = IpcCreateLicenseFromTemplateID(pcTil-&gt;aTi[0].wszID, 
                                    0, 
                                    NULL, 
                                    &amp;pLicenseHandle);
    
    DWORD dwEncryptionMode = IPC_ENCRYPTION_PACKAGE_AES128_ECB;
    
    hr = IpcSetLicenseProperty(pLicenseHandle, 
                           false,
                           IPC_LI_PREFERRED_ENCRYPTION_PACKAGE, 
                           &amp;dwEncryptionMode);
    
 

 





<!--HONumber=Apr16_HO3-->

