---
title: OptionGroup.Height property (Access)
keywords: vbaac10.chm10837
f1_keywords:
- vbaac10.chm10837
ms.prod: access
api_name:
- Access.OptionGroup.Height
ms.assetid: f0b715ff-a1d4-4040-59e6-818705042691
ms.date: 02/21/2019
ms.localizationpriority: medium
---


# OptionGroup.Height property (Access)

Gets or sets the height of the specified object in [twips](../language/glossary/vbe-glossary.md#twip). Read/write **Integer**.


## Syntax

_expression_.**Height**

_expression_ A variable that represents an **[OptionGroup](Access.OptionGroup.md)** object.


## Remarks

For report controls, you can set the **Height** property when you print or preview a report only by using a macro or an event procedure specified in a section's **OnFormat** event property setting.

Microsoft Access automatically sets the **Height** property when you create or size a control or when you size a window in form Design view or report Design view.

The height of controls is measured from the center of their borders so that controls with different border widths align correctly. 




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]