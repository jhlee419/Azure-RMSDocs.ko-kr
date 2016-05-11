---
# required metadata

title: Rights Management 공유 응용 프로그램&colon; 버전 릴리스 기록 | Azure RMS
description:
keywords:
author: cabailey
manager: mbaldwin
ms.date: 04/28/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: 6751bd90-959f-4eba-91ed-6588ac983762

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: esaggese
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Rights Management 공유 응용 프로그램: 버전 릴리스 기록
Rights Management 팀에서는 픽스 및 새 기능을 위해 Rights Management 공유 응용 프로그램을 정기적으로 업데이트합니다. 다음 정보를 통해 새로운 기능이나 릴리스 변경을 확인합니다. 가장 최근 릴리스가 먼저 나열됩니다.

2015년 1월 1일 이전 버전은 목록에 없습니다.

> [!NOTE]
> RMS 공유 응용 프로그램에 대한 의견이나 질문이 있으면 [AskIPTeam](mailto:AskIPTeam@microsoft.com?subject=RMS%20sharing%20app:%20Feedback%20or%20question)에 전자 메일 메시지를 보냅니다.

## 버전 1.0.2004.0
**릴리스 날짜**: 2015년 12월 11일

**수정 사항**:

-   파일 소유자와 **공동 소유자** 권한 수준의 사용자만 파일 보호를 해제할 수 있습니다. 이전에는 소유자와 **공동 작성자** 및 **공동 소유자** 권한 수준의 사용자가 파일 보호를 해제할 수 있었습니다.

-   RMS 보호된 읽기 전용 **.ptif** 파일을 생성하기 위한 **.tif** 파일(및 .tiff 파일)에 대한 기본 보호입니다.

-   오류 메시지 개선(정확도 및 명확성).

-   내용 암호화 및 암호 해독에 대한 성능 개선

**새로운 기능**:

-   비관리자 설치를 지원하므로 표준 사용자가 RMS 공유 응용 프로그램을 설치할 수 있습니다.

    Office 2010을 실행하는 표준 사용자에 대한 몇 가지 제한 사항이 있습니다. 자세한 내용은 [Rights Management 공유 응용 프로그램 다운로드 및 설치](install-sharing-app.md) 사용자 지침에서 [로컬 관리자가 아닌 사용자가 Office 2010을 사용하는 경우](install-sharing-app.md#if-you-are-not-a-local-administrator-and-use-office-2010) 섹션을 참조하세요.

## 버전 1.0.1908.0
**릴리스 날짜**: 2015년 9월 16일

**수정 사항**:

-   최신 인증을 사용하는 응용 프로그램에서 Microsoft 로그인 도우미에 대한 종속성도 제거하는 Azure RMS에 대한 MFA(다단계 인증)를 지원합니다.

    자세한 내용은 [Azure 권한 관리에 대한 요구 사항](../get-started/requirements-azure-rms.md)에서 [MFA(Multi-Factor Authentication) 및 Azure RMS](../get-started/requirements-azure-ad.md#multi-factor-authentication-mfa-and-azure-rms) 섹션을 참조하세요.

## 버전 1.0.1784.0
**릴리스 날짜**: 2015년 7월 30일

**수정 사항**:

-   권한 정책 템플릿의 기본 새로고침 간격을 7일에서 1일로 줄입니다.

-   발생 빈도가 낮고 사소한 버그

## 버전 1.0.1770.0
**릴리스 날짜**: 2015년 4월 25일

**수정 사항**:

-   이제 소유자 및 공동 소유자만 보호를 제거할 수 있습니다. 공동 작성자는 보호를 제거할 수 없습니다.

-   이제 네트워크 공유에 있는 파일을 보호할 수 있습니다.

**새로운 기능**:

-   문서 추적 및 해지를 지원합니다. 자세한 내용은 [RMS 공유 응용 프로그램을 사용하는 경우 문서 추적 및 취소](sharing-app-track-revoke.md)를 참조하세요.

-   **보호 상태로 공유**선택 시의 템플릿 지원:

    -   이제 템플릿을 선택할 수 있습니다.

    -   슬라이더 대신 템플릿과 사용자 지정 권한이 포함된 목록 상자가 표시됩니다.

    -   **모든 장치에서 사용 허용** 과 **사용 제한 적용**옵션은 이제 표시되지 않습니다. 대신 파일 형식에 따라 **일반 보호** 가 자동으로 선택됩니다.

    자세한 내용은 [Rights Management 공유 응용 프로그램에 대한 대화 상자 옵션](sharing-app-dialog-box.md)을 참조하세요.

## 버전 1.0.1667.0
**릴리스 날짜**: 2015년 1월 19일

**수정 사항**:

-   RMS 공유 앱 PPDF 뷰어에서 중국어 글꼴을 지원합니다.

-   오류 처리 및 메시징이 향상되었습니다.

-   응용 프로그램의 최신 버전을 다운로드할 수 있을 때 자동 업데이트 알림에서의 문제가 해결되었습니다.

**새로운 기능**:

-   **조직 내의 여러 메일 도메인 지원**: AD RMS를 사용하며 조직의 사용자에게 여러 메일 도메인이 있는 경우 이 업데이트를 통해 사용자가 다른 도메인의 조직 사용자에 의해 보호된 콘텐츠를 사용할 수 있습니다. 자세한 내용은 [Rights Management 공유 응용 프로그램 관리자 가이드](sharing-app-admin-guide.md)에서 [AD RMS에만 해당: 조직 내의 여러 메일 도메인 지원](sharing-app-admin-guide.md#ad-rms-only-support-for-multiple-email-domains-within-your-organization) 섹션을 참조하세요.



<!--HONumber=Apr16_HO3-->

