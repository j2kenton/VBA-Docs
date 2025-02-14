---
title: PostItem.IsConflict property (Outlook)
keywords: vbaol11.chm1564
f1_keywords:
- vbaol11.chm1564
ms.prod: outlook
api_name:
- Outlook.PostItem.IsConflict
ms.assetid: b2f65ec7-da76-29d1-421c-01163a0aadfe
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# PostItem.IsConflict property (Outlook)

Returns a **Boolean** that determines if the item is in conflict. Read-only.


## Syntax

_expression_. `IsConflict`

_expression_ A variable that represents a [PostItem](Outlook.PostItem.md) object.


## Remarks

Whether or not an item is in conflict is determined by the state of the application. For example, when a user is offline and tries to access an online folder the action will fail. In this scenario, the  **IsConflict** property will return **True**.

If  **True**, the specified item is in conflict.


## See also


[PostItem Object](Outlook.PostItem.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]