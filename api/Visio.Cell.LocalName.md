---
title: Cell.LocalName property (Visio)
keywords: vis_sdr.chm10113860
f1_keywords:
- vis_sdr.chm10113860
ms.prod: visio
api_name:
- Visio.Cell.LocalName
ms.assetid: 596bf196-6bbc-32f0-e508-03cdf4969a7f
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Cell.LocalName property (Visio)

Returns the local name of a cell. Read-only.


## Syntax

_expression_.**LocalName**

_expression_ A variable that represents a **[Cell](Visio.Cell.md)** object.


## Return value

String


## Remarks

A cell has both a local name and a universal name. The local name differs according to the locale for which Microsoft Windows is installed on the user's system. The universal name is the same regardless of locale.

To get the universal name of a cell, use the  **Name** property.

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]