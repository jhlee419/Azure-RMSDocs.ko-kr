---
# required metadata

title: Visual Studio 구성 | Azure RMS
description: RMS SDK 2.1을 사용하도록 Visual Studio 프로젝트를 구성하는 방법에 대한 지침입니다.
keywords:
author: bruceperlerms
manager: mbaldwin
ms.date: 04/28/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: 8581e996-79b4-4ffc-a63e-2236c83dc954

# optional metadata

#ROBOTS:
audience: developer
#ms.devlang:
ms.reviewer: shubhamp
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

﻿# Visual Studio 구성

이 항목에는 권한 관리 서비스 SDK 2.1을 사용하도록 Visual Studio 프로젝트를 구성하는 방법에 대한 지침이 포함되어 있습니다.

## 필수 구성 요소

-   [SDK 설치](create-your-first-rights-aware-application.md)

**지침**

### 1단계: RMS SDK 2.1을 사용하도록 Visual Studio 프로젝트 구성

이러한 지침은 Microsoft Visual Studio 2010에 해당합니다. 다른 버전의 Microsoft Visual Studio를 사용하는 경우 설정 대화 상자가 약간 다르게 나타날 수도 있습니다.

이러한 지침은 네이티브 32비트 응용 프로그램 빌드에 적용됩니다.

1.  Visual Studio 2010 프로젝트에 RMS SDK 2.1 포함 디렉터리를 추가합니다.

    **구성 속성**에서 **VC++ 디렉터리**를 선택하고 RMS SDK 2.1 포함 디렉터리인 **$(MSIPCSDKDIR)\\inc**를 **포함 디렉터리** 필드에 추가합니다.

    ![구성 속성 포함 디렉터리 필드](../media/include_directories.png)

2.  Visual Studio 2010 프로젝트에 RMS SDK 2.1 라이브러리 디렉터리를 추가합니다.

    **구성 속성**에서 **VC++ 디렉터리**를 선택하고 RMS SDK 2.1 라이브러리 디렉터리를 해당 플랫폼의 **라이브러리 디렉터리** 필드에 추가합니다.

    -   Win32의 경우 **$(MSIPCSDKDIR)\\lib**를 사용합니다.
    -   x64의 경우 **$(MSIPCSDKDIR)\\lib\\x64**를 사용합니다.

    ![구성 속성 라이브러리 디렉터리 필드](../media/library_directories.png)

3.  RMS SDK 2.1 라이브러리 파일을 Visual Studio 2010 종속성으로 추가합니다.

    **링커**에서 **입력**을 선택하고 RMS SDK 2.1 라이브러리 파일인 **Msipc.lib** 및 **Msipc\_s.lib**를 **추가 종속성** 필드에 추가합니다.

    ![링커 라이브러리 종속성 필드](../media/additional_dependencies.png)

4.  RMS SDK 2.1 DLL(동적 연결 라이브러리)을 지연 로드된 DLL로 추가합니다.

    **링커**에서 **입력**을 선택하고 RMS SDK 2.1 DLL 파일인 **Msipc.dll**을 **지연 로드된 Dll** 필드에 추가합니다.

    ![링커 지연 로드된 라이브러리 필드](../media/delay_loaded.png)

5.  결과 이진에 대한 버전 정보를 만듭니다.

    **솔루션 탐색기**에서 **리소스 파일**을 선택하고 이진 이름을 **OriginalFileName** 필드에 추가합니다.

    ![솔루션 탐색기 리소스 파일 필드](../media/original_file_name.png)

### 관련 항목

* [사용 방법](how-to-use-msipc.md)
* [SDK 설치](create-your-first-rights-aware-application.md)
 

 





<!--HONumber=Apr16_HO3-->

