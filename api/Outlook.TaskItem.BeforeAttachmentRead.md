---
title: TaskItem.BeforeAttachmentRead event (Outlook)
ms.prod: outlook
api_name:
- Outlook.TaskItem.BeforeAttachmentRead
ms.assetid: 298eaece-9633-637b-3055-572d77fa3811
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# TaskItem.BeforeAttachmentRead event (Outlook)

Occurs before an attachment associated with an instance of the parent object is read from the file system, an attachment stream, or an **[Attachment](Outlook.Attachment.md)** object.


## Syntax

_expression_. `BeforeAttachmentRead`( `_Attachment_` , `_Cancel_` )

_expression_ A variable that represents a [TaskItem](Outlook.TaskItem.md) object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Attachment_|Required| **Attachment**|The **Attachment** to be read.|
| _Cancel_|Required| **Boolean**|Set to  **True** to cancel the operation; otherwise, set to **False** to allow the **Attachment** to be read.|

## See also


[TaskItem Object](Outlook.TaskItem.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]