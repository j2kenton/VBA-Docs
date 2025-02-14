---
title: ToggleButton.OnGotFocus property (Access)
keywords: vbaac10.chm11751
f1_keywords:
- vbaac10.chm11751
ms.prod: access
api_name:
- Access.ToggleButton.OnGotFocus
ms.assetid: bcc774c8-7766-942d-b37d-d4c96dd84911
ms.date: 02/23/2019
ms.localizationpriority: medium
---


# ToggleButton.OnGotFocus property (Access)

Sets or returns the value of the **On Got Focus** box in the Properties window of the specified object. Read/write **String**.


## Syntax

_expression_.**OnGotFocus**

_expression_ A variable that represents a **[ToggleButton](Access.ToggleButton.md)** object.


## Remarks

This property is helpful for programmatically changing the action that Microsoft Access takes when an event is triggered. For example, between event calls you may want to change an expression's parameters, or switch from an event procedure to an expression or macro, depending on the circumstances under which the event was triggered. 

The **GotFocus** event occurs when the object receives the focus.

The **OnGotFocus** value will be one of the following, depending on the selection chosen in the Choose Builder window (accessed by choosing the **Build** button next to the **On Got Focus** box in the object's Properties window):

- If you choose Expression Builder, the value will be =_expression_, where _expression_ is the expression from the Expression Builder window.
    
- If you choose Macro Builder, the value is the name of the macro. 
    
- If you choose Code Builder, the value will be [Event Procedure]. 
    
If the **On Got Focus** box is blank, the property value is an empty string.


## Example

The following example prints the value of the **OnGotFocus** property in the Immediate window for the button named **OK** on the **Order Entry** form.


```vb
Debug.Print Forms("Order Entry").Controls("OK").OnGotFocus
```


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]