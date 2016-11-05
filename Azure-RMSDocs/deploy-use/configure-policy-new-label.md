---
title: "새 레이블을 만드는 방법 | Azure Information Protection"
description: "Azure Information Protection은 사용자 지정 가능한 기본 레이블과 함께 제공되지만 사용자의 Information Protection 표시줄에 표시되는 고유의 레이블을 만들 수도 있습니다."
manager: mbaldwin
ms.date: 09/25/2016
ms.topic: article
ms.prod: 
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: 1b45faa5-0c9c-40d6-910a-f117e7b6e8a3
translationtype: Human Translation
ms.sourcegitcommit: ebb11148718f22c79bb49c82b9855f5e6f2a5b18
ms.openlocfilehash: 5cf6237f33d0818c8411cbb5126fc825c3c411d7


---

# Azure Information Protection에 대한 새 레이블을 만드는 방법

>*적용 대상: Azure Information Protection*

Azure Information Protection은 사용자 지정 가능한 기본 레이블과 함께 제공되지만 사용자의 Information Protection 표시줄에 표시되는 고유의 레이블을 만들 수도 있습니다.

추가 수준의 분류가 필요한 경우 새 레이블 또는 새 하위 레이블을 기존 레이블에 추가할 수 있습니다. 예를 들어 [기본 정책](configure-policy-default.md)에 있는 **Secret**(비밀) 레이블에는 하위 레이블이 포함되어 있습니다.

다음 지침을 사용하여 Azure Information Protection 정책에 새 레이블을 추가할 수 있습니다.

1. 아직 그렇게 하지 않은 경우에는, 새 브라우저 창에서 전역 관리자로 [Azure Portal](https://portal.azure.com)에 로그인한 다음 **Azure Information Protection** 블레이드로 이동합니다. 
    
    예를 들어 허브 메뉴에서 **추가 서비스**를 클릭하고 필터 상자에 **Information**을 입력합니다. **Azure Information Protection**을 선택합니다.

2. **Azure Information Protection** 블레이드에서 다음 중 하나를 수행합니다.

    - 새 레이블을 만들려면: **Add a new label**(새 레이블 추가)을 클릭합니다.

    - 새 하위 레이블을 만들려면: 마우스 오른쪽 단추를 클릭하거나 하위 레이블을 만들려는 레이블에 대한 상황에 맞는 메뉴(**...**)를 선택하고 **Add a sub-label**(하위 레이블 추가)을 클릭합니다.

3. **Label**(레이블) 또는 **Sub-label**(하위 레이블) 블레이드에서 이 새 레이블에 대한 옵션을 선택하고 **Save**(저장)를 클릭합니다.

    > [!NOTE]
    >보호 설정에 대한 자세한 내용은 [보호를 적용하도록 레이블을 구성하는 방법](configure-policy-protection.md)을 참조하세요.

4. 변경 내용을 사용자에게 제공하려면 **Azure Information Protection** 블레이드에서 **Publish**(게시)를 클릭합니다.

## 다음 단계

Azure Information Protection 정책 구성에 대해 자세히 알아보려면 [조직의 정책 구성](configure-policy.md#configuring-your-organization-s-policy) 섹션의 링크를 사용하세요.  





<!--HONumber=Sep16_HO4-->

