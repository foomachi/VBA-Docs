---
title: Window.ZoomLock property (Visio)
keywords: vis_sdr.chm11651460
f1_keywords:
- vis_sdr.chm11651460
ms.prod: visio
api_name:
- Visio.Window.ZoomLock
ms.assetid: 9f962982-27e0-a427-de5f-ed4d3ee04e73
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Window.ZoomLock property (Visio)

Determines whether zooming is disabled in a Microsoft Visio drawing window. Read/write.


## Syntax

_expression_. `ZoomLock`

_expression_ A variable that represents a **[Window](Visio.Window.md)** object.


## Return value

Boolean


## Remarks

Zooming (**False**) is the default Visio behavior. You can use the **ZoomLock** property to prevent zooming in any Visio drawing window, including page, master, and group windows. Attempting to set the **ZoomLock** for other windows, including stencil windows, ShapeSheet windows, and icon windows, will throw an exception.

The  **ZoomLock** property setting is valid only for a given window at run time, and is not persisted (saved) in either the Visio document or the registry.

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]