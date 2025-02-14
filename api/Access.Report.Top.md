---
title: Report.Top property (Access)
keywords: vbaac10.chm13728
f1_keywords:
- vbaac10.chm13728
ms.prod: access
api_name:
- Access.Report.Top
ms.assetid: badaa1a0-44ef-c2cd-64fa-8450add21d69
ms.date: 02/26/2019
ms.localizationpriority: medium
---


# Report.Top property (Access)

You can use the **Top** property to specify an object's location on a form or report. Read/write **Long**.


## Syntax

_expression_.**Top**

_expression_ A variable that represents a **[Report](Access.Report.md)** object.


## Remarks

In Visual Basic, use a numeric expression to set the value of this property. Values are expressed in [twips](../language/glossary/vbe-glossary.md#twip).

For reports, the **Top** property setting is the amount that the current section is offset from the top of the page. This property setting is expressed in twips. You can use this property to specify how far down the page you want a section to print in the section's **Format** event procedure.


## Example

The following example checks the **Top** property setting for the current report. If the value is less than the minimum margin setting, the **NextRecord** and **PrintSection** properties are set to **False**. The section doesn't advance to the next record, and the next section isn't printed.

```vb
Sub Detail1_Format(Cancel As Integer, FormatCount As Integer) 
Const conTopMargin = 1880 
' Don't advance to next record or print next section 
' if Top property setting is less than 1880 twips. 
 If Me.Top < conTopMargin Then 
 Me.NextRecord = False 
 Me.PrintSection = False 
 End If 
End Sub
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]