---
title: Shape.Import method (Visio)
keywords: vis_sdr.chm11216355
f1_keywords:
- vis_sdr.chm11216355
ms.prod: visio
api_name:
- Visio.Shape.Import
ms.assetid: 07c858ee-0bbc-5ac1-37be-1e853cdf2361
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Shape.Import method (Visio)

Imports a file into the current document.


## Syntax

_expression_.**Import** (_FileName_)

_expression_ A variable that represents a **[Shape](Visio.Shape.md)** object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _FileName_|Required| **String**|The name of the file to import; must be a fully qualified path.|

## Return value

Shape


## Remarks

The  **Import** method imports the file specified by _FileName_ onto a page, or into a master or group.

The file name extension indicates which import filter to use. If the filter is not installed, the  **Import** method returns an error. The **Import** method uses the default preference settings for the specified filter and does not prompt the user for non-default arguments.


## Example

This Microsoft Visual Basic for Applications (VBA) macro shows how to use the  **Import** method to import a bitmap image onto the drawing page. This example assumes that there is a file with the name _sampleImage.bmp_ on drive C of your computer.


```vb
Public Sub Import_Example() 
 
 ActivePage.Import ("C:\sampleImage.bmp") 
 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]