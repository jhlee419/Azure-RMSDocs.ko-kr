---
title: "응용 프로그램 테스트 | Azure RMS"
description: "테스트를 위해 응용 프로그램을 설치하는 방법에 대한 지침입니다."
keywords: 
author: lleonard-msft
ms.author: alleonar
manager: mbaldwin
ms.date: 02/23/2017
ms.topic: article
ms.prod: 
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: E480D8D6-F070-43D1-B2B0-6921459C3437
audience: developer
ms.reviewer: shubhamp
ms.suite: ems
ms.openlocfilehash: c1705015efbe038b577c63286813bc560e62b148
ms.sourcegitcommit: 93124ef58e471277c7793130f1a82af33dabcea9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/11/2018
---
# <a name="testing-your-application"></a>응용 프로그램 테스트

이 항목에서는 응용 프로그램 테스트를 위해 설치하는 방법에 대한 지침을 제공합니다.

## <a name="instructions"></a>지침

### <a name="step-1-setup-for-testing"></a>1단계: 테스트를 위한 설치

Windows Server에서 실행 중인 Azure RMS 또는 RMS 서버에서 테스트할 수 있으며, Azure RMS에서 테스트를 시작한 다음 배포에 필요한 경우 RMS 서버에서 테스트하는 것이 좋습니다.

1. Azure RMS에서 테스트하는 방법에 대해서는 [방법: ADAL 인증 사용](how-to-use-adal-authentication.md) 항목을 참조하세요.
2. RMS 서버에서 테스트하는 방법에 대해서는 [방법: RMS 서버 설치 및 구성](how-to-install-and-configure-an-rms-server.md) 항목을 참조하세요.
3. 다음에서는 Developer 런타임을 설치하는 방법을 설명합니다.

   응용 프로그램을 테스트할 컴퓨터에 Rights Management Service Client 2.1이 설치되어 있어야 합니다.
   - 개발 컴퓨터 이외의 컴퓨터에서 응용 프로그램을 테스트하는 경우 [AD RMS 클라이언트 다운로드 페이지](http://www.microsoft.com/en-us/download/details.aspx?id=38396)에서 해당 컴퓨터에 RMS Client 2.1을 설치할 수 있습니다.
   - 개발 컴퓨터에서 응용 프로그램을 테스트하는 경우 권한 관리 서비스 SDK 2.1을 이미 설치한 상태여야 합니다. 지금은 RMS Client 2.1이 자동으로 설치됩니다.

    RMS SDK 2.1을 설치하는 방법에 대한 자세한 내용은 [SDK 설치](install-the-rms-sdk.md)를 참조하세요.

## <a name="remarks"></a>설명

이 항목의 지침은 일부에 불과합니다. RMS Client 2.1을 구성하는 방법에 대한 자세한 내용은 [RMS Client 2.1 배포 참고 사항](https://technet.microsoft.com/en-us/library/jj159267(WS.10).aspx) 항목을 참조하세요.

### <a name="related-topics"></a>관련 항목

* [RMS 서버 설치 및 구성 방법](how-to-install-and-configure-an-rms-server.md)
* [방법: ADAL 인증 사용](how-to-use-adal-authentication.md)
* [SDK 설치](install-the-rms-sdk.md)
* [RMS Client 2.1 배포 참고 사항](https://technet.microsoft.com/en-us/library/jj159267(WS.10).aspx)

[!INCLUDE[Commenting house rules](../includes/houserules.md)]