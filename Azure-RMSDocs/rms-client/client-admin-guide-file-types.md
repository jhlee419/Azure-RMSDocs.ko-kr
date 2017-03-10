---
title: "Azure Information Protection에서 지원하는 파일 형식"
description: "지원되는 파일 형식, 파일 이름 확장명 및 Windows용 Azure Information Protection 클라이언트에 대한 책임이 있는 관리자의 보호 수준에 대한 기술 세부 정보입니다."
author: cabailey
ms.author: cabailey
manager: mbaldwin
ms.date: 02/23/2017
ms.topic: article
ms.prod: 
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: 
ms.reviewer: esaggese
ms.suite: ems
translationtype: Human Translation
ms.sourcegitcommit: 2131f40b51f34de7637c242909f10952b1fa7d9f
ms.openlocfilehash: 107bac4e318c08d4fdc6d24fc88a6f7cbe5c0a74
ms.lasthandoff: 02/24/2017


---


# <a name="file-types-supported-by-the-azure-information-protection-client"></a>Azure Information Protection 클라이언트에서 지원하는 파일 형식

>*적용 대상: Active Directory Rights Management 서비스, Azure Information Protection, Windows 10, Windows 8.1, Windows 8, Windows 7 SP1*

Azure Information Protection 클라이언트는 문서 및 전자 메일에 다음을 적용할 수 있습니다.

- 분류만

- 분류 및 보호

- 보호만

다음 정보를 사용하여 지원되는 파일 형식, 다양한 보호 수준과 기본 보호 수준을 변경하는 방법, 분류 및 보호에서 자동으로 제외되는(건너뜀) 파일을 확인할 수 있습니다.

## <a name="file-types-supported-for-classification-only"></a>분류만 지원되는 파일 형식

다음 파일 형식의 경우 분류만 지원됩니다. 다른 파일 형식은 보호도 수행해야 분류가 지원됩니다.

- **Microsoft Visio**: .vsdx, .vsdm, .vssx, .vssm, .vsd, .vdw, .vst

- **Microsoft Project**: .mpp, .mpt

- **Microsoft Publisher**: .pub

- **Microsoft Office 97, Office 2010, Office 2003**: .xls, .xlt, .doc, .dot, .ppt, .pps, .pot

- **Microsoft XPS**: .xps .oxps

- **이미지**: .jpg, .jpe, .jpeg, .jif, .jfif, .jfi.png, .tif, .tiff

- **SolidWorks**: .sldprt, .slddrw, .sldasm

- **Autodesk Design Review 2013**: .dwfx

- **Adobe Photoshop**: .psd

- **디지털 네거티브**: .dng

## <a name="file-types-supported-for-protection"></a>보호가 지원되는 파일 형식

Azure Information Protection 클라이언트는 다음 표에서 설명하는 것처럼 각기 다른 두 수준의 보호를 지원합니다.

|보호 유형|네이티브|제네릭|
|----------------------|----------|-----------|
|설명|텍스트, 이미지, Microsoft Office(Word, Excel, PowerPoint) 파일, .pdf 파일 및 Rights Management 서비스를 지원하는 기타 응용 프로그램 파일 형식의 경우 기본 보호는 권한 적용 및 암호화를 모두 포함하는 강력한 보호 수준을 제공합니다.|기타 모든 응용 프로그램 및 파일 형식의 경우 일반 보호는 사용자가 파일을 열 권한이 있는지를 확인하는 인증 및 .pfile 파일 형식을 사용하는 파일 캡슐화 기능이 모두 포함된 보호 수준을 제공합니다.|
|보호|파일은 다음과 같은 방식으로 완벽하게 암호화되며 보호가 적용됩니다.<br /><br />- 보호된 콘텐츠를 렌더링하기 전에 메일을 통해 파일을 받았거나 파일 또는 공유 권한을 통해 파일 액세스 권한을 부여받은 사용자가 정상적으로 인증을 해야 합니다.<br /><br />- 또한 Azure Information Protection 뷰어(보호된 텍스트, 이미지 파일의 경우)나 연결된 응용 프로그램(지원되는 기타 모든 파일 형식의 경우)에서 콘텐츠를 렌더링할 때는 파일 보호 시 콘텐츠 소유자가 설정한 사용 권한 및 정책이 완전하게 적용됩니다.|파일 보호는 다음과 같은 방식으로 적용됩니다.<br /><br />- 보호된 콘텐츠를 렌더링하기 전에 파일을 열 권한이 있으며 파일 액세스 권한을 부여받은 사용자가 정상적으로 인증해야 합니다. 권한 부여가 실패하면 파일이 열리지 않습니다.<br /><br />- 콘텐츠 소유자가 설정한 사용 권한 및 정책이 표시되어 해당하는 사용 정책의 권한 있는 사용자를 알려 줍니다.<br /><br />- 지원되지 않는 응용 프로그램의 경우 파일을 열고 액세스하는 권한 있는 사용자의 감사 로깅이 수행되기는 하지만 사용 권한은 적용되지 않습니다.|
|파일 형식에 대한 기본값|이 보호 수준은 다음 파일 형식에 대한 기본 보호 수준입니다.<br /><br />- 텍스트 및 이미지 파일<br /><br />- Microsoft Office(Word, Excel, PowerPoint) 파일<br /><br />- Portable Document Format(.pdf)<br /><br />자세한 내용은 [지원되는 파일 형식 및 파일 이름 확장명](#supported-file-types-for-protection-and-their-file-name-extensions) 섹션을 참조하세요.|이 수준은 전체 보호를 통해 지원되지 않는 .vsdx, .rtf 등의 기타 모든 파일 형식에 대한 기본 보호 수준입니다.|

Azure Information Protection 클라이언트가 적용하는 기본 보호 수준을 변경할 수 있습니다. 기본 수준을 일반 수준으로 변경하거나 그 반대로 변경할 수 있으며, Azure Information Protection 클라이언트가 보호를 적용하지 않도록 차단할 수도 있습니다. 자세한 내용은 이 문서에서 [파일의 기본 보호 수준 변경](#changing-the-default-protection-level-of-files) 섹션을 참조하세요.

관리자가 구성한 레이블을 선택할 때 이 데이터 보호를 자동으로 적용할 수도 있고, [권한 수준](../deploy-use/configure-usage-rights.md#rights-included-in-permissions-levels)을 사용하여 사용자 보호 설정을 직접 지정할 수도 있습니다. 

### <a name="supported-file-types-for-protection-and-their-file-name-extensions"></a>보호 및 해당 파일 이름 확장명에 대해 지원되는 파일 형식
다음 표에는 Azure Information Protection 클라이언트에서 고유하게 지원되는 파일 형식이 나와 있습니다. 이러한 파일 형식의 경우 기본 보호를 적용하면 원래 파일 이름 확장명이 변경되며 해당 파일은 읽기 전용이 됩니다.

일반 수준으로 보호되는 파일의 경우에는 원래 파일 이름 확장명이 항상 .pfile로 변경됩니다.

> [!WARNING]
> 파일 이름 확장명을 검사한 다음 그에 따라 작업을 수행하는 방화벽, 웹 프록시 또는 보안 소프트웨어를 사용하는 경우에는 이러한 새 파일 이름 확장명을 지원하도록 방화벽, 웹 프록시 또는 보안 소프트웨어를 다시 구성해야 할 수 있습니다.

|원래 파일 이름 확장명|보호된 파일 이름 확장명|
|--------------------------------|-------------------------------------|
|.txt|.ptxt|
|.xml|.pxml|
|.jpg|.pjpg|
|.jpeg|.ppng|
|.pdf|.ppdf|
|.png|.ppng|
|.tif|.ptif|
|.tiff|.ptiff|
|.bmp|.pbmp|
|.gif|.pgif|
|.jpe|.pjpe|
|.jfif|.pjfif|
|.jt|.pjt|


다음 표에는 Azure Information Protection 클라이언트에서 Microsoft Office 앱에 대해 고유하게 지원하는 파일 형식이 나와 있습니다. 이러한 파일의 경우에는 Rights Management 서비스를 통해 파일을 보호한 후에도 파일 이름 확장명이 동일하게 유지됩니다.

|Office에서 지원하는 파일 형식|Office에서 지원하는 파일 형식|
|----------------------------------|----------------------------------|
|.doc<br /><br />.docm<br /><br />.docx<br /><br />.dot<br /><br />.dotm<br /><br />.dotx<br /><br />.potm<br /><br />.potx<br /><br />.pps<br /><br />.ppsm<br /><br />.ppsx<br /><br />.ppt<br /><br />.pptm|.pptx<br /><br />.thmx<br /><br />.xla<br /><br />.xlam<br /><br />.xls<br /><br />.xlsb<br /><br />.xlt<br /><br />.xlsm<br /><br />.xlsx<br /><br />.xltm<br /><br />.xltx<br /><br />.xps|

### <a name="changing-the-default-protection-level-of-files"></a>파일의 기본 보호 수준 변경
레지스트리를 편집하여 Azure Information Protection 클라이언트가 파일을 보호하는 방식을 변경할 수 있습니다. 예를 들어 기본 보호를 지원하는 파일을 Azure Information Protection 클라이언트에서 일반적으로 보호하도록 강제 지정할 수 있습니다.

이러한 작업을 수행해야 하는 이유는 다음과 같습니다.

-   기본 보호를 지원하는 응용 프로그램을 사용하지 않더라도 모든 사용자가 파일을 열 수 있도록 설정

-   파일 이름 확장명을 기준으로 하여 파일에 대해 작업을 수행하며, .pfile 파일 이름 확장명을 수용하도록 다시 구성할 수는 있지만 기본 보호를 위해 여러 파일 이름 확장명을 수용하도록 다시 구성할 수는 없는 보안 시스템 수용

마찬가지로 일반 보호가 기본적으로 적용되는 파일에 대해 Azure Information Protection 클라이언트가 기본 보호를 적용하도록 강제 지정할 수 있습니다. 부 개발자가 작성한 LOB(기간 업무) 응용 프로그램이나 ISV(Independent Software Vendor)에서 구매한 응용 프로그램 등 RMS API를 지원하는 응용 프로그램을 사용하는 경우 이러한 작업을 수행할 수 있습니다.

Azure Information Protection 클라이언트가 파일 보호를 차단하도록, 즉 기본 보호 또는 일반 보호를 적용하지 않도록 강제 지정할 수도 있습니다. 예를 들어 콘텐츠를 처리하려면 특정 파일을 열 수 있어야 하는 자동화된 응용 프로그램이나 서비스를 사용하는 경우 이러한 작업을 수행해야 할 수 있습니다. 특정 파일 형식에 대한 보호를 차단하면 사용자가 Azure Information Protection 클라이언트를 사용하여 해당 파일 형식의 파일을 보호할 수 없습니다. 이러한 파일을 보호하려고 하면 관리자가 보호를 차단했으므로 파일을 보호하기 위한 작업을 취소해야 한다는 메시지가 표시됩니다.

기본적으로 기본 보호가 적용되는 모든 파일에 대해 Azure Information Protection 클라이언트가 일반 보호를 적용하도록 구성하려면 다음 레지스트리를 편집합니다. FileProtection 키가 없으면 직접 만들어야 합니다.

1.  **HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\FileProtection**: 이름이 *인 새 키를 만듭니다.

    이 설정은 임의의 파일 이름 확장명이 지정된 파일을 나타냅니다.

2.  새로 추가한 키 HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\FileProtection\\\*에서 데이터 값이 **Pfile**인 새 문자열 값(REG_SZ) **Encryption**을 만듭니다.

    이 설정을 지정하면 Azure Information Protection 클라이언트가 일반 보호를 적용합니다.

이 두 설정을 사용하면 Azure Information Protection 클라이언트가 특정 파일 이름 확장명을 사용하는 모든 파일에 일반 보호를 적용합니다. 이러한 결과를 원하는 경우에는 추가 구성을 수행할 필요가 없습니다. 그러나 계속 기본적으로 보호되도록 특정 파일 형식에 대해 예외를 정의할 수 있습니다. 이렇게 하려면 각 파일 형식에 대해 추가로&3;개 레지스트리를 편집해야 합니다.

1.  **HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\FileProtection**: 파일 이름 확장명(앞의 마침표는 제외)이 이름으로 지정된 새 키를 추가합니다.

    예를 들어 파일 이름 확장명이 .docx인 파일의 경우 **DOCX**키를 만듭니다.

2.  새로 추가된 파일 형식 키(예: **HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\FileProtection\DOCX**)에서 값이 **0**인 새 DWORD 값 **AllowPFILEEncryption**을 만듭니다.

3.  새로 추가된 파일 형식 키(예: **HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\FileProtection\DOCX**)에서 값이 **Native**인 새 문자열 값 **Encryption**을 만듭니다.

이러한 설정을 사용하는 경우 파일 이름 확장명이 .doxc인 파일(Azure Information Protection 클라이언트에 의해 기본적으로 보호됨)을 제외한 모든 파일이 일반적으로 보호됩니다.

기본 보호를 지원하며 Azure Information Protection 클라이언트에서 일반적으로 보호하지 않도록 지정하기 위해 예외로 정의하려는 다른 파일 형식에 대해 이&3;단계를 반복합니다.

다음 값을 지원하는 **Encryption** 문자열의 값을 변경하여 다른 시나리오에서도 비슷하게 레지스트리를 편집할 수 있습니다.

-   **Pfile**: 일반 보호

-   **Native**: 기본 보호

-   **Off**: 보호 차단

자세한 내용은 개발자 지침에서 [파일 API 구성](../develop/file-api-configuration.md)을 참조하세요. 개발자를 위한 이 설명서에서는 일반 보호를 "PFile"이라고 합니다. 

## <a name="file-types-that-are-excluded-from-classification-and-protection-by-the-azure-information-protection-client"></a>Azure Information Protection 클라이언트에 의해 분류 및 보호에서 제외되는 파일 형식

사용자가 컴퓨터 작업에 중요한 파일을 변경하지 못하게 하기 위해 일부 파일 형식 및 폴더가 분류 및 보호에서 자동으로 제외됩니다. 사용자가 이러한 파일을 분류하거나 보호하려고 하면 제외된다는 메시지가 표시됩니다.

- **제외되는 파일 형식**:.lnk,.exe,.com,.cmd,.bat,.dll,.ini,.pst,.sca,.drm,.sys,.cpl,.inf,.drv,.dat,.tmp,.msp,.msi,.pdb,.jar

- **제외되는 폴더**: 
    - Windows
    - 프로그램 파일(\Program Files 및 \Program Files (x86))
    - \ProgramData 
    - \AppData(모든 사용자용)




## <a name="next-steps"></a>다음 단계
Azure Information Protection 클라이언트에서 지원하는 파일 형식을 파악했으므로 다음에서 이 클라이언트를 지원하는 데 필요할 수 있는 추가 정보를 참조하세요.

- [클라이언트 파일 및 사용 현황 로깅](client-admin-guide-files-and-logging.md)

- [문서 추적](client-admin-guide-document-tracking.md)

- [PowerShell 명령](client-admin-guide-powershell.md)

[!INCLUDE[Commenting house rules](../includes/houserules.md)]
