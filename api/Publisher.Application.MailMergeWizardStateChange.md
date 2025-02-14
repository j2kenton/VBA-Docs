---
title: Application.MailMergeWizardStateChange event (Publisher)
keywords: vbapb10.chm268435479
f1_keywords:
- vbapb10.chm268435479
ms.prod: publisher
api_name:
- Publisher.Application.MailMergeWizardStateChange
ms.assetid: 3d3fcdaa-af51-0a28-ff25-f2b92deceaf6
ms.date: 06/05/2019
ms.localizationpriority: medium
---


# Application.MailMergeWizardStateChange event (Publisher)

Occurs when a user changes from a specified step to a specified step in the Mail Merge Wizard.


## Syntax

_expression_.**MailMergeWizardStateChange** (_Doc_, _FromState_)

_expression_ A variable that represents an **[Application](Publisher.Application.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
|_Doc_|Required| **Document**|The mail merge main document.|
|_FromState_|Required| **Integer**|The Mail Merge Wizard step from which a user is moving.|

## Remarks

To access the **Application** object events, declare an **Application** object variable in the General Declarations section of a code module, and then set the variable equal to the **Application** object for which you want to access events.

For information about using events with the Microsoft Publisher **Application** object, see [Using events with the Application object](../publisher/Concepts/using-events-with-the-application-object-publisher.md).

## Example

This example displays a message when a users moves from step three of the Mail Merge Wizard to step four. Based on the user's answer to the message, the user will either continue on to step four or return to step three.

```vb
Private Sub MailMergeApp_MailMergeWizardStateChange(ByVal Doc As Document, _ 
 ByVal FromState As Long) 
 
 Select Case FromState 
 Case 1 
 MsgBox "Now you will build your publication merge " & _ 
 "by adding fields to your publication." 
 Case 2 
 MsgBox "Now you will see your publication " & _ 
 "merged with the records in the data source." 
 Case 3 
 MsgBox "Now you will complete the mail merge process." 
 End Select 
 
End Sub
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]