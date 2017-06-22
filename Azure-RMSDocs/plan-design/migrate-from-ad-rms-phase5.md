---
title: "AD RMS-Azure Information Protection 마이그레이션 - 5단계"
description: "AD RMS에서 Azure Information Protection으로 마이그레이션하는 과정의 다섯 번째 단계로, AD RMS에서 Azure Information Protection으로 마이그레이션 10~12단계가 포함됩니다."
author: cabailey
ms.author: cabailey
manager: mbaldwin
ms.date: 04/18/2017
ms.topic: article
ms.prod: 
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: d51e7bdd-2e5c-4304-98cc-cf2e7858557d
ms.reviewer: esaggese
ms.suite: ems
ms.openlocfilehash: e07e9252837fe17c84ce17c3b1fc8e20734190fd
ms.sourcegitcommit: 237ce3a0cc4921da5a08ed5753e6491403298194
translationtype: HT
---
# <a name="migration-phase-5---post-migration-tasks"></a>마이그레이션 5단계 - 마이그레이션 후 작업

>*적용 대상: Active Directory Rights Management Services, Azure Information Protection, Office 365*


AD RMS에서 Azure Information Protection으로 마이그레이션 5단계에는 다음 정보를 사용합니다. 이러한 절차는 [AD RMS에서 Azure Information Protection으로 마이그레이션](migrate-from-ad-rms-to-azure-rms.md)의 10~12단계를 설명합니다.

## <a name="step-10-deprovison-ad-rms"></a>10단계. AD RMS 프로비전 해제

온-프레미스 권한 관리 인프라에서 컴퓨터를 검색하지 못하게 하려면 Active Directory에서 SCP(서비스 연결 지점)를 제거합니다. 이는 레지스트리에서 마이그레이션 스크립트를 실행하는 등의 방법으로 구성한 리디렉션 때문에 마이그레이션한 기존 클라이언트에 대한 선택 사항입니다. 그러나 SCP를 제거하면 마이그레이션이 완료되고 모두 Azure Rights Management Service로 연결되어야 할 때 새 클라이언트 및 잠재적으로 RMS 관련 서비스 및 도구가 SCP를 찾지 못합니다. 

SCP를 제거하려면 도메인 엔터프라이즈 관리자로 로그인하고 다음 절차를 사용합니다.

1. Active Directory Rights Management Services 콘솔에서 AD RMS 클러스터를 마우스 오른쪽 단추로 클릭하고 **속성**을 클릭합니다.

2. **SCP** 탭을 클릭합니다.

3. **SCP 변경** 확인란을 선택합니다.

4. **현재 SCP 제거**를 클릭하고 **확인**을 클릭합니다.

이제 [시스템 상태 보고서의 요청](https://technet.microsoft.com/library/ee221012%28v=ws.10%29.aspx), [ServiceRequest 테이블](http://technet.microsoft.com/library/dd772686%28v=ws.10%29.aspx) 또는 [보호된 콘텐츠에 대한 사용자 액세스 감사](http://social.technet.microsoft.com/wiki/contents/articles/3440.ad-rms-frequently-asked-questions-faq.aspx) 등을 확인하여 AD RMS 서버에서 활동을 모니터링합니다. 

RMS 클라이언트가 이러한 서버와 더 이상 통신하지 않으며 클라이언트가 Azure Information Protection을 성공적으로 사용하고 있는지 확인한 다음, 이러한 서버에서 AD RMS 서버 역할을 제거할 수 있습니다. 전용 서버를 사용하는 경우, 일정 기간 동안 서버를 종료한 후 이러한 서버를 다시 시작해야 하는 문제가 보고되지 않았는지 확인하는 준비 단계를 거쳐 클라이언트가 Azure Information Protection을 사용하지 않는 이유를 조사할 때 서비스가 중단되지 않도록 할 수 있습니다.

AD RMS 서버 프로비전을 해제한 후에는 Azure 클래식 포털에서 템플릿을 검토하고 통합하여 사용자가 더 적은 수의 템플릿 중에서 선택하거나, 템플릿을 다시 구성하거나, 새 템플릿을 추가할 기회를 제공할 수 있습니다. 이때 기본 템플릿을 게시하는 것도 좋습니다. 자세한 내용은 [Azure Rights Management 서비스용 사용자 지정 템플릿 구성](../deploy-use/configure-custom-templates.md)을 참조하세요.

>[!IMPORTANT]
> 이 마이그레이션이 끝나면 AD RMS 클러스터를 Azure Information Protection 및 HYOK(Hold Your Own Key) 옵션에 사용할 수 없습니다. 현재 구현된 리디렉션 때문에 Azure Information Protection 레이블에 HYOK를 사용하기로 한 경우 사용하는 AD RMS 클러스터의 라이선스 URL은 마이그레이션한 클러스터의 라이선스 URL과 달라야 합니다.

## <a name="step-11-remove-onboarding-controls"></a>11단계. 온보딩 컨트롤 제거

모든 기존 클라이언트를 Azure Information Protection으로 마이그레이션했으면 계속 온보딩 컨트롤을 사용하거나 마이그레이션 프로세스를 위해 만든 **AIPMigrated** 그룹을 유지할 이유가 없습니다. 

먼저 온보딩 컨트롤을 제거한 다음 **AIPMigrated** 그룹과 리디렉션을 배포하기 위해 만든 모든 소프트웨어 배포 작업을 삭제할 수 있습니다.

온보딩 컨트롤을 제거하려면:

1. PowerShell 세션에서 Azure Rights Management 서비스에 연결하고 메시지가 표시되면 전역 관리자 자격 증명을 지정합니다.

        Connect-Aadrmservice

2. 다음 명령을 실행하고 **Y**를 입력하여 확인합니다.

        Set-AadrmOnboardingControlPolicy -UseRmsUserLicense $False

3. 더 이상 온보딩 컨트롤이 설정되어 있지 않은지 확인합니다.

        Get-AadrmOnboardingControlPolicy

    출력에서 **License**가 **False**를 표시해야 하고, **SecurityGroupOjbectId**에 대해 표시되는 GUID가 없습니다.

## <a name="step-12-re-key-your-azure-information-protection-tenant-key"></a>12단계. Azure Information Protection 테넌트 키 다시 입력
이 단계는 AD RMS 배포에서 RMS 암호화 모드 1을 사용한 경우 마이그레이션이 완료되었을 때 필요합니다. 키를 다시 입력하면 RMS 암호화 모드 2를 사용하는 새 테넌트 키가 생성되기 때문입니다. 암호화 모드 1에서 Azure RMS를 사용하는 방식은 마이그레이션 프로세스 중에만 지원됩니다.

이 단계는 선택 사항이지만 RMS 암호화 모드 2에서 실행 중이었을 때 마이그레이션이 완료된 경우에 권장됩니다. 이 시나리오의 키 다시 입력은 Azure Information Protection 테넌트 키를 AD RMS 키에 대한 잠재적인 보안 위반으로부터 보호하는 데 도움이 됩니다.

Azure Information Protection 테넌트 키를 다시 입력하면("키 롤링"이라고도 함) 새 키가 만들어지고 원래 키는 보관됩니다. 하지만 한 키에서 다른 키로 바로 이동되지 않고 몇 주 이상이 걸립니다. 따라서 원래 키에 대해 의심스러운 위반이 발생할 때까지 기다리지 말고, 마이그레이션이 완료되는 즉시 Azure Information Protection 테넌트 키를 다시 입력합니다.

Azure Information Protection 테넌트 키를 다시 입력하려면

- Microsoft에서 관리하는 테넌트 키인 경우: [Microsoft 지원](../get-started/information-support.md#to-contact-microsoft-support)에 문의하여 **AD RMS에서 마이그레이션 후 Azure Information Protection 키 다시 입력 요청에 관한 Azure Information Protection 지원 케이스**를 엽니다. 자신이 Azure Information Protection 테넌트의 관리자임을 증명해야 하고, 이 프로세스를 확인하는 데 며칠이 걸린다는 것을 이해해야 합니다. 표준 지원 요금이 적용됩니다. 테넌트 키 다시 입력은 무료 지원 서비스가 아닙니다.

- 사용자가 관리하는 테넌트 키인 경우(BYOK): Azure Key Vault에서 Azure Information Protection 테넌트에 사용 중인 키를 다시 입력한 다음 [Use-AadrmKeyVaultKey](/powershell/aadrm/vlatest/use-aadrmkeyvaultkey) cmdlet을 다시 실행하여 새 키 URL을 지정합니다. 

Azure Information Protection 테넌트 키 관리에 대한 자세한 내용은 [Azure Rights Management 테넌트 키에 대한 작업](../deploy-use/operations-tenant-key.md)을 참조하세요.

## <a name="next-steps"></a>다음 단계

이제는 마이그레이션을 완료했으므로 [배포 로드맵](deployment-roadmap.md)을 검토하여 필요할 수 있는 다른 배포 작업을 확인합니다.

[!INCLUDE[Commenting house rules](../includes/houserules.md)]