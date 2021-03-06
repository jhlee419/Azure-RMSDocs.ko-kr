---
title: "Azure Information Protection의 기본 정책"
description: "Azure Information Protection에 대한 기본 정책을 구성하는 방법을 설명합니다. 기본 정책을 수정하는 경우 이러한 값을 참조하여 정책을 기본값으로 반환할 수 있습니다."
author: cabailey
ms.author: cabailey
manager: mbaldwin
ms.date: 03/09/2018
ms.topic: article
ms.prod: 
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: 671281c8-f0d1-42b6-aae3-681d1821e2cf
ms.openlocfilehash: d89acde3a2d9e4db529c429fdedf2f3ed05e2fe5
ms.sourcegitcommit: 335c854eb5c6f387a9369d4b6f1e22160517e6ce
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/12/2018
---
# <a name="the-default-azure-information-protection-policy"></a>기본 Azure Information Protection 정책

>*적용 대상: Azure Information Protection*

다음 정보를 사용하여 Azure Information Protection에 대한 기본 정책을 구성하는 방법을 이해할 수 있습니다.

관리자가 처음 Azure Portal을 사용하여 Azure Information Protection 서비스에 연결하면 해당 테넌트에 대한 기본 정책이 만들어집니다. 경우에 따라 Microsoft에서 기본 정책을 변경할 수 있지만, 기본 정책이 수정되기 전에 이미 서비스를 사용하고 있었던 경우 이전 버전의 기본 정책을 구성하고 프로덕션 환경에 배포했을 수 있으므로 이전 버전의 기본 정책은 업데이트되지 않습니다.

다음 값을 참조하여 정책을 기본값으로 되돌리거나 정책을 최신 값으로 업데이트할 수 있습니다.

## <a name="current-default-policy"></a>현재 기본 정책

이 버전의 기본 정책은 2017년 7월 31일에 생성되었습니다.

이 기본 정책은 Azure Rights Management 서비스를 활성화할 때 생성되며, 2018년 2월부터 새 테넌트에 적용됩니다. 자세한 내용은 블로그 게시물 알림인 [Improvements to the protection stack in Azure Information Protection](https://cloudblogs.microsoft.com/enterprisemobility/2018/03/08/improvements-to-the-protection-stack-in-azure-information-protection)(Azure Information Protection의 보호 스택에 대한 개선 사항)을 참조하세요.

이 기본 정책은 정책을 만들기 전에 수동으로 [서비스를 활성화](activate-service.md)하는 경우에도 생성됩니다. 

이 서비스가 활성화되지 않은 경우 기본 정책에서는 다음 하위 레이블에 대한 보호를 구성하지 않습니다.

- **Confidential \ All Employees**

- **Confidential \ Recipients Only**

- **Highly Confidential \ All Employees** 

- **Highly Confidential \ Recipients Only** 

이러한 하위 레이블이 보호를 자동으로 구성하지 않은 경우 기본 정책이 [이전 기본 정책](#default-policy-before-july-31-2017)과 동일하게 유지됩니다.

보호가 **모든 직원** 하위 레벨에 적용된 경우 Azure Portal에서 레이블로 자동 전환되는 기본 템플릿을 사용하여 보호가 구성됩니다. 이 템플릿에 대한 자세한 내용은 [Azure Information Protection 템플릿 구성 및 관리](configure-policy-templates.md)를 참조하세요.

2017년 8월 30일부터 이 버전의 기본 정책에는 여러 언어의 레이블 이름 및 설명이 포함됩니다. 

#### <a name="more-information-about-the-recipients-only-sublabel"></a>받는 사람만 하위 레벨에 대한 자세한 내용

Outlook에서만 이 레이블이 표시됩니다. Word, Excel, PowerPoint 또는 파일 탐색기에서는 이 레이블이 표시되지 않습니다. 

이 레이블을 선택하면 Outlook 전달 금지 옵션이 자동으로 메일에 적용됩니다. 사용자가 지정한 받는 사람은 메일을 전달할 수 없으며 콘텐츠를 복사 또는 인쇄하거나 첨부 파일을 저장할 수 없습니다.


### <a name="labels"></a>레이블입니다.

|Label|도구 설명|설정|
|-------------------------------|---------------------------|-----------------|
|개인|비즈니스와 관계없는 개인 전용 데이터입니다.|**사용**: 켜기 <br /><br />**색**: 연한 녹색<br /><br />**시각적 표시**: 끄기 <br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|Public|공개 사용을 위해 특별히 준비 및 승인된 비즈니스 데이터입니다.|**사용**: 켜기 <br /><br />**색**: 녹색<br /><br />**시각적 표시**: 끄기<br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|일반|공개 사용을 목적으로 하지 않는 비즈니스 데이터입니다. 그러나 필요에 따라 외부 파트너와 이 데이터를 공유할 수 있습니다. 회사 내부 전화번호부, 조직도, 내부 표준 및 대부분의 내부 통신을 예로 들 수 있습니다.|**사용**: 켜기 <br /><br />**색**: 파란색 <br /><br />**시각적 표시**: 끄기<br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|기밀|권한이 없는 사람들과 공유되는 경우 비즈니스에 피해를 야기할 수 있는 중요한 비즈니스 데이터입니다. 계약, 보안 보고서, 예측 요약 및 판매 계정 데이터를 예로 들 수 있습니다.|**사용**: 켜기 <br /><br />**색**: 주황색<br /><br />**시각적 표시**: 끄기<br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|극비|권한이 없는 사람들과 공유할 경우 비즈니스에 피해를 야기하는 매우 중요한 비즈니스 데이터입니다. 직원 및 고객 정보, 암호, 소스 코드 및 미리 공개된 재무 보고서 등을 예로 들 수 있습니다.|**사용**: 켜기 <br /><br />**색**: 빨간색<br /><br />**시각적 표시**: 끄기<br /><br />**조건**: 없음<br /><br />**보호**: 없음|


### <a name="sublabels"></a>하위 레이블

|Label|도구 설명|설정|
|-------------------------------|---------------------------|-----------------|
|기밀 \ 모든 직원|모든 직원에게 전체 권한을 허용하는 보호가 필요한 기밀 데이터입니다. 데이터 소유자는 콘텐츠를 추적하고 해지할 수 있습니다.|**사용**: 켜기 <br /><br />**시각적 표시**: 바닥글(문서 및 메일)<br /><br />기밀로 분류됨<br /><br />**조건**: 없음<br /><br />**보호**: Azure(클라우드 키)[[1]](#footnote-1)|
|기밀 \ 모든 사람(보호되지 않음)|보호가 필요하지 않은 데이터입니다. 이 옵션은 적절한 비즈니스 근거를 바탕으로 신중히 사용하세요.|**사용**: 켜기 <br /><br />**시각적 표시**: 바닥글(문서 및 메일)<br /><br />기밀로 분류됨 <br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|Confidential \ Recipients Only|보호가 필요하며 받는 사람만 볼 수 있는 기밀 데이터입니다.|**사용**: 켜기 <br /><br />**시각적 표시**: 바닥글(메일)<br /><br />기밀로 분류됨 <br /><br />**조건**: 없음<br /><br />**보호**: 사용자 정의 권한 설정(미리 보기), Outlook에서 전달 금지 적용|
|극비 \ 모든 직원|모든 직원에게 이 콘텐츠에 대한 보기, 편집 및 회신 권한을 허용하는 극비 데이터입니다. 데이터 소유자는 콘텐츠를 추적하고 해지할 수 있습니다.|**사용**: 켜기 <br /><br />**시각적 표시**: 바닥글(문서 및 메일)<br /><br />극비로 분류됨<br /><br />**조건**: 없음<br /><br />**보호**: Azure(클라우드 키)[[2]](#footnote-2)|
|극비 \ 모든 사람(보호되지 않음)|보호가 필요하지 않은 데이터입니다. 이 옵션은 적절한 비즈니스 근거를 바탕으로 신중히 사용하세요.|**사용**: 켜기 <br /><br />**시각적 표시**: 바닥글(문서 및 메일)<br /><br />극비로 분류됨<br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|Highly Confidential \ Recipients Only|보호가 필요하며 받는 사람만 볼 수 있는 극비 데이터입니다.|**사용**: 켜기 <br /><br />**시각적 표시**: 바닥글(메일)<br /><br />극비로 분류됨 <br /><br />**조건**: 없음<br /><br />**보호**: 사용자 정의 권한 설정(미리 보기), Outlook에서 전달 금지 적용|

###### <a name="footnote-1"></a>각주 1
보호 권한은 [기본 템플릿](configure-policy-templates.md#default-templates), **기밀 \ 모든 직원**의 보호 권한과 일치합니다.

###### <a name="footnote-2"></a>각주 2 
보호 권한은 [기본 템플릿](configure-policy-templates.md#default-templates), **극비 \ 모든 직원**의 보호 권한과 일치합니다.


### <a name="information-protection-bar"></a>Information Protection 표시줄

|Setting|값|
|-------------------------------|---------------------------|
|제목|민감도|
|도구 설명|이 콘텐츠의 현재 레이블입니다. 이 설정은 통해 조직 내부 또는 외부의 권한이 없는 사람들과 이 콘텐츠를 공유할 경우 비즈니스에 대한 위험을 식별합니다.|


### <a name="settings"></a>설정

|Setting|값|
|-------------------------------|---------------------------|
|All documents and emails must have a label (applied automatically or by users)(모든 문서와 메일에 레이블이 있어야 함(자동으로 적용되거나 사용자에 의해 적용됨))|꺼짐|
|Select the default label(기본 레이블 선택)|없음|
|Users must provide justification to set a lower classification label, remove a label, or remove protection(더 낮은 분류 레이블을 설정하거나, 레이블 또는 보호를 제거할 때 사용자가 근거를 제공해야 함)|꺼짐|
|For email messages with attachments, apply a label that matches the highest classification of those attachments(첨부 파일이 있는 메일 메시지의 경우 해당 첨부 파일의 최고 분류와 일치하는 레이블 적용)|꺼짐|
|Azure Information Protection 클라이언트 "추가 정보" 웹 페이지에 대한 사용자 지정 URL 제공|비어 있음|


## <a name="default-policy-before-july-31-2017"></a>2017년 7월 31일 이전의 기본 정책

이 정책의 설명에서는 보호가 필요한 데이터를 참조하고 데이터 추적 및 해지도 참조합니다. 정책에서는 이러한 레이블에 대해 이 보호를 구성하지 않으므로 이 설명을 준수하기 위한 추가 단계를 수행해야 합니다. 예를 들어 보호를 적용하거나 DLP(데이터 손실 방지) 솔루션을 사용하도록 레이블을 구성합니다. 문서 추적 사이트를 사용하여 문서를 추적하고 해지하려면 먼저 문서를 Azure Rights Management 서비스로 보호해야 하며, 문서를 보호한 사람이 추적해야 합니다. 


### <a name="labels"></a>레이블입니다.

|Label|도구 설명|설정|
|-------------------------------|---------------------------|-----------------|
|개인|비즈니스와 관계없는 개인 전용 데이터입니다.|**사용**: 켜기 <br /><br />**색**: 연한 녹색<br /><br />**시각적 표시**: 끄기 <br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|Public|공개 사용을 위해 특별히 준비 및 승인된 비즈니스 데이터입니다.|**사용**: 켜기 <br /><br />**색**: 녹색<br /><br />**시각적 표시**: 끄기<br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|일반|공개 사용을 목적으로 하지 않는 비즈니스 데이터입니다. 그러나 필요에 따라 외부 파트너와 이 데이터를 공유할 수 있습니다. 회사 내부 전화번호부, 조직도, 내부 표준 및 대부분의 내부 통신을 예로 들 수 있습니다.|**사용**: 켜기 <br /><br />**색**: 파란색 <br /><br />**시각적 표시**: 끄기<br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|기밀|권한이 없는 사람들과 공유되는 경우 비즈니스에 피해를 야기할 수 있는 중요한 비즈니스 데이터입니다. 계약, 보안 보고서, 예측 요약 및 판매 계정 데이터를 예로 들 수 있습니다.|**사용**: 켜기 <br /><br />**색**: 주황색<br /><br />**시각적 표시**: 끄기<br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|극비|권한이 없는 사람들과 공유할 경우 비즈니스에 피해를 야기하는 매우 중요한 비즈니스 데이터입니다. 직원 및 고객 정보, 암호, 소스 코드 및 미리 공개된 재무 보고서 등을 예로 들 수 있습니다.|**사용**: 켜기 <br /><br />**색**: 빨간색<br /><br />**시각적 표시**: 끄기<br /><br />**조건**: 없음<br /><br />**보호**: 없음|


### <a name="sublabels"></a>하위 레이블

|Label|도구 설명|설정|
|-------------------------------|---------------------------|-----------------|
|기밀 \ 모든 직원|모든 직원에게 전체 권한을 허용하는 보호가 필요한 기밀 데이터입니다. 데이터 소유자는 콘텐츠를 추적하고 해지할 수 있습니다.|**사용**: 켜기 <br /><br />**시각적 표시**: 바닥글(문서 및 메일)<br /><br />기밀로 분류됨<br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|기밀 \ 모든 사람(보호되지 않음)|보호가 필요하지 않은 데이터입니다. 이 옵션은 적절한 비즈니스 근거를 바탕으로 신중히 사용하세요.|**사용**: 켜기 <br /><br />**시각적 표시**: 바닥글(문서 및 메일)<br /><br />기밀로 분류됨 <br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|극비 \ 모든 직원|모든 직원에게 이 콘텐츠에 대한 보기, 편집 및 회신 권한을 허용하는 극비 데이터입니다. 데이터 소유자는 콘텐츠를 추적하고 해지할 수 있습니다.|**사용**: 켜기 <br /><br />**시각적 표시**: 바닥글(문서 및 메일)<br /><br />극비로 분류됨<br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|극비 \ 모든 사람(보호되지 않음)|보호가 필요하지 않은 데이터입니다. 이 옵션은 적절한 비즈니스 근거를 바탕으로 신중히 사용하세요.|**사용**: 켜기 <br /><br />**시각적 표시**: 바닥글(문서 및 메일)<br /><br />극비로 분류됨<br /><br />**조건**: 없음<br /><br />**보호**: 없음|

### <a name="information-protection-bar"></a>Information Protection 표시줄

|Setting|값|
|-------------------------------|---------------------------|
|제목|민감도|
|도구 설명|이 콘텐츠의 현재 레이블입니다. 이 설정은 통해 조직 내부 또는 외부의 권한이 없는 사람들과 이 콘텐츠를 공유할 경우 비즈니스에 대한 위험을 식별합니다.|


### <a name="settings"></a>설정

|Setting|값|
|-------------------------------|---------------------------|
|All documents and emails must have a label (applied automatically or by users)(모든 문서와 메일에 레이블이 있어야 함(자동으로 적용되거나 사용자에 의해 적용됨))|꺼짐|
|Select the default label(기본 레이블 선택)|없음|
|Users must provide justification to set a lower classification label, remove a label, or remove protection(더 낮은 분류 레이블을 설정하거나, 레이블 또는 보호를 제거할 때 사용자가 근거를 제공해야 함)|꺼짐|
|For email messages with attachments, apply a label that matches the highest classification of those attachments(첨부 파일이 있는 메일 메시지의 경우 해당 첨부 파일의 최고 분류와 일치하는 레이블 적용)|꺼짐|
|Azure Information Protection 클라이언트 "추가 정보" 웹 페이지에 대한 사용자 지정 URL 제공|비어 있음|

## <a name="default-policy-before-march-21-2017"></a>2017년 3월 21일 이전의 기본 정책

### <a name="labels"></a>레이블입니다.

|Label|도구 설명|설정|
|-------------------------------|---------------------------|-----------------|
|개인|개인 전용. 이 데이터는 조직에서 모니터링하지 않습니다. 개인 정보는 비즈니스 관련 데이터를 포함할 수 없습니다.|**사용**: 켜기 <br /><br />**색**: 연한 녹색<br /><br />**시각적 표시**: 끄기 <br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|Public|이 정보는 내부용이며, 회사 내부 또는 외부의 모든 사용자가 사용할 수 있습니다.|**사용**: 켜기 <br /><br />**색**: 녹색<br /><br />**시각적 표시**: 끄기<br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|Internal|이 정보는 모든 직원이 사용할 수 있으며, 권한 있는 고객 및 비즈니스 파트너와 공유할 수 있는 광범위한 내부 비즈니스 데이터를 포함합니다. 내부 정보의 예로는 회사 정책과 대부분의 내부 통신이 있습니다.|**사용**: 켜기 <br /><br />**색**: 파란색 <br /><br />**시각적 표시**: 바닥글(문서 및 메일): <br /><br />민감도: 내부<br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|기밀|이 데이터는 민감한 비즈니스 정보를 포함합니다. 권한 없는 사용자에게 이 데이터를 노출하면 조직이 해를 입을 수 있습니다. 기밀 정보의 예로는 직원 정보, 개별 고객 프로젝트 또는 계약 및 판매 계정 데이터가 있습니다.|**사용**: 켜기 <br /><br />**색**: 주황색<br /><br />**시각적 표시**: 바닥글(문서 및 메일):<br /><br /> 민감도: 기밀<br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|비밀|이 데이터는 보호해야 하는 매우 민감한 비즈니스 정보를 포함합니다. 권한 없는 사용자에게 비밀 데이터를 노출하면 조직이 심각한 해를 입을 수 있습니다. 비밀 정보의 예로는 개인 식별 정보, 고객 레코드, 소스 코드, 사전 발표된 재무 보고서 등이 있습니다.|**사용**: 켜기 <br /><br />**색**: 빨간색<br /><br />**시각적 표시**: 바닥글(문서 및 메일):<br /><br /> 민감도: 비밀<br /><br />**조건**: 없음<br /><br />**보호**: 없음|


### <a name="sublabels"></a>하위 레이블

|Label|도구 설명|설정|
|-------------------------------|---------------------------|-----------------|
|비밀 \ 모든 회사|이 데이터는 모든 회사 직원에게 허용되는 민감한 비즈니스 정보를 포함합니다.|**사용**: 켜기 <br /><br />**시각적 표시**: 끄기<br /><br />**조건**: 없음<br /><br />**보호**: 없음|
|비밀 \ 내 그룹|이 데이터는 직원 그룹에만 허용되는 민감한 비즈니스 정보를 포함합니다.|**사용**: 켜기 <br /><br />**시각적 표시**: 끄기<br /><br />**조건**: 없음<br /><br />**보호**: 없음|

### <a name="information-protection-bar"></a>Information Protection 표시줄

|Setting|값|
|-------------------------------|---------------------------|
|제목|민감도|
|도구 설명|정보 민감도는 사용자가 회사 내부 또는 외부의 권한 없는 사용자에게 정보를 노출하는 위험을 식별할 수 있도록 네 가지 고유 수준(공개, 내부, 기밀, 비밀)으로 구성됩니다.|


### <a name="settings"></a>설정

|Setting|값|
|-------------------------------|---------------------------|
|All documents and emails must have a label (applied automatically or by users)(모든 문서와 메일에 레이블이 있어야 함(자동으로 적용되거나 사용자에 의해 적용됨))|꺼짐|
|Select the default label(기본 레이블 선택)|없음|
|Users must provide justification to set a lower classification label, remove a label, or remove protection(더 낮은 분류 레이블을 설정하거나, 레이블 또는 보호를 제거할 때 사용자가 근거를 제공해야 함)|꺼짐|
|Azure Information Protection 클라이언트 "추가 정보" 웹 페이지에 대한 사용자 지정 URL 제공|비어 있음|


## <a name="next-steps"></a>다음 단계

Azure Information Protection 정책 구성에 대해 자세히 알아보려면 [조직의 정책 구성](configure-policy.md#configuring-your-organizations-policy) 섹션의 링크를 사용하세요. 

[!INCLUDE[Commenting house rules](../includes/houserules.md)]