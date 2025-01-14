---
title: Call Stack dialog box
keywords: vbui6.chm181029
f1_keywords:
- vbui6.chm181029
ms.prod: office
ms.assetid: 304c94c2-4aea-d11d-892f-5cadd24aef8a
ms.date: 11/26/2018
ms.localizationpriority: medium
---


# Call Stack dialog box

![Call stack](../../../images/calls_ZA01201584.gif)

Displays a list of currently active procedure calls during [break mode](../../Glossary/vbe-glossary.md#break-mode). When executing code in a procedure, that procedure is added to a list of active procedure calls. Each time a procedure calls another procedure, it is added to the list. Called procedures are removed from the list when execution returns to the calling procedure. Procedures called from the [Immediate window](immediate-window.md) are also added to the calls list.

The following table describes the dialog box options.

|Option|Description|
|:-----|:----------|
|**Project Module Function**|Lists the procedures.|
|**Show**|Moves the insertion point to the location where the call was made, and turns on the Call Stack indicator ![Call stack indicator](../../../images/wcallst_ZA01201809.gif).|

## See also

- [Dialog boxes](../dialog-boxes.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]