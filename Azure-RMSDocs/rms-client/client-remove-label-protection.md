---
title: "Azure Information Protection 레이블 제거"
description: "Azure Information Protection에 의해 레이블이 지정되었거나 Rights Management로 보호된 파일에서 분류 레이블 및 보호를 제거하기 위한 지침입니다."
author: cabailey
ms.author: cabailey
manager: mbaldwin
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: 
ms.reviewer: eymanor
ms.suite: ems
ms.openlocfilehash: b7651b39760f9ebf71970ec744d553a71f5e9c9c
ms.sourcegitcommit: 832d3ef5f9c41d6adb18a8cf5304f6048cc7252e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/24/2017
---
# <a name="user-guide-remove-labels-and-protection-from-files-and-emails-that-have-been-labeled-by-azure-information-protection-or-protected-by-rights-management"></a>사용자 가이드; Azure Information Protection에 의해 레이블이 지정되었거나 Rights Management로 보호된 파일 및 전자 메일에서 분류 레이블 및 보호를 제거합니다.

>*적용 대상: Active Directory Rights Management 서비스, Azure Information Protection, Windows 10, Windows 8.1, Windows 8, Windows 7 SP1*

[Azure Information Protection 클라이언트가 컴퓨터에 설치되어 있으면](install-client-app.md) 파일 및 전자 메일에서 분류 레이블 및 보호를 제거할 수 있습니다.

제거하는 레이블이 보호를 적용하도록 구성된 경우 파일에서 보호도 제거됩니다. 레이블을 제거하는 이유를 기록하라는 메시지가 표시될 수 있습니다.

> [!IMPORTANT]
> 보호를 제거하려면 파일의 소유자이거나 보호를 제거하기 위한 권한(Rights Management 추출 권한 또는 모든 권한)이 부여되어야 합니다.

다른 레이블 또는 다른 보호 설정 집합을 선택하려는 경우에는 레이블 또는 보호를 제거할 필요가 없습니다. 대신 새 레이블을 선택하고, 필요한 경우 사용자 지정 권한을 정의할 수 있습니다. 

Office 데스크톱 앱 **Word**, **Excel**, **PowerPoint**, **Outlook** 내에서 Office 문서 및 전자 메일을 만들거나 편집할 때 해당 문서 및 전자 메일에서 레이블 및 보호를 제거할 수 있습니다. 

**파일 탐색기**를 사용하여 레이블 및 보호를 제거할 수도 있습니다. 파일 탐색기는 추가적인 파일 형식을 지원하며, 여러 파일에서 한 번에 레이블 및 보호를 제거할 수 있는 편리한 방법입니다.

## <a name="using-office-apps-to-remove-labels-and-protection-from-documents-and-emails"></a>Office 앱을 사용하여 문서 및 전자 메일에서 레이블 및 보호 제거

Information Protection 표시줄에서 **레이블 제거** 아이콘을 클릭합니다.

![Azure Information Protection 표시줄 - 레이블 삭제](../media/delete-label.png)

**레이블 삭제** 아이콘을 즉시 사용할 수 있는 경우가 아니면 먼저 **레이블 편집** 아이콘을 클릭합니다.

![Azure Information Protection 표시줄 - 레이블 편집](../media/edit-label.png)

> [!NOTE]
> Office 앱에 이 Information Protection 표시줄이 표시되지 않는 경우
> 
> - Azure Information Protection 클라이언트를 [설치](install-client-app.md)하지 않았거나 클라이언트가 [보호 전용 모드](client-protection-only-mode.md)로 실행되고 있습니다.

## <a name="using-file-explorer-to-remove-labels-and-protection-from-files"></a>파일 탐색기를 사용하여 파일에서 레이블 및 보호 제거

파일 탐색기를 사용할 때는 파일 하나, 여러 개 또는 폴더에서 빠르게 레이블 및 보호를 제거할 수 있습니다. 폴더를 선택하면 해당 폴더의 모든 파일 및 하위 폴더가 자동으로 선택됩니다. 

1.  파일 탐색기에서 파일 하나/여러 개 또는 폴더를 선택합니다. 마우스 오른쪽 단추를 클릭하고 **분류 및 보호**를 선택합니다.

2. 레이블을 제거하려면: **분류 및 보호 - Azure Information Protection** 대화 상자에서 **레이블 삭제**를 클릭합니다. 레이블이 보호를 적용하도록 구성된 경우 보호가 자동으로 제거됩니다.

3. 단일 파일에서 사용자 지정 보호를 제거하려면: **분류 및 보호 - Azure Information Protection** 대화 상자에서 **사용자 지정 권한으로 보호** 옵션을 선택 취소합니다.
    
4. 여러 파일에서 사용자 지정 보호를 제거하려면: **분류 및 보호 - Azure Information Protection** 대화 상자에서 **사용자 지정 권한 제거** 옵션을 클릭합니다.

5. **적용**을 클릭하고 **작업 완료** 메시지가 표시될 때까지 기다린 후 결과를 확인합니다. 그런 다음 **닫기**를 클릭합니다.


## <a name="other-instructions"></a>기타 지침
Azure Information Protection 사용자 가이드의 사용 방법 지침:

- [원하는 옵션을 선택하](client-user-guide.md#what-do-you-want-to-do)세요.


[!INCLUDE[Commenting house rules](../includes/houserules.md)]