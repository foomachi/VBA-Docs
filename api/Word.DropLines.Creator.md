---
title: DropLines.Creator property (Word)
keywords: vbawd10.chm104988821
f1_keywords:
- vbawd10.chm104988821
ms.prod: word
api_name:
- Word.DropLines.Creator
ms.assetid: 1c8081db-916f-0291-b3a2-f163b664da68
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# DropLines.Creator property (Word)

Returns a 32-bit integer that indicates the application in which the specified object was created. Read-only  **Long**.


## Syntax

_expression_.**Creator**

_expression_ A variable that represents a '[DropLines](Word.DropLines.md)' object.


## Remarks

If the object was created in Microsoft Word, the **Creator** property returns the hexadecimal number 4D535744, which represents the string "MSWD". This property was primarily designed to be used on the Macintosh, where each application has a four-character creator code. For example, Word has the creator code MSWD. For more information about this property, consult the language reference Help included with Microsoft Office for Mac.


## See also


[DropLines Object](Word.DropLines.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]