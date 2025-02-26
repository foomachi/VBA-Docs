---
title: OptionButton.SpecialEffect property (Access)
keywords: vbaac10.chm10586
f1_keywords:
- vbaac10.chm10586
ms.prod: access
api_name:
- Access.OptionButton.SpecialEffect
ms.assetid: 33dd01c0-0ee0-640d-d8f3-f7c3590aeb90
ms.date: 02/26/2019
ms.localizationpriority: medium
---


# OptionButton.SpecialEffect property (Access)

You can use the **SpecialEffect** property to specify whether special formatting will apply to the specified object. Read/write **Byte**.


## Syntax

_expression_.**SpecialEffect**

_expression_ A variable that represents an **[OptionButton](Access.OptionButton.md)** object.


## Remarks

The **SpecialEffect** property uses the following settings.

|Setting|Visual Basic|Description|
|:-----|:-----|:-----|
|Flat|0|The object appears flat and has the system's default colors or custom colors that were set in Design view.|
|Raised|1|The object has a highlight on the top and left and a shadow on the bottom and right.|
|Sunken|2|The object has a shadow on the top and left and a highlight on the bottom and right.|
|Etched|3|The object has a sunken line surrounding the control.|
|Shadowed|4|The object has a shadow below and to the right of the control.|
|Chiseled|5|The object has a sunken line below the control.|

The **SpecialEffect** property setting affects related property settings for the **BorderStyle**, **BorderColor**, and **BorderWidth** properties. For example, if the **SpecialEffect** property is set to Raised, the settings for the **BorderStyle**, **BorderColor**, and **BorderWidth** properties are ignored. In addition, changing or setting the **BorderStyle**, **BorderColor**, and **BorderWidth** properties may cause Microsoft Access to change the **SpecialEffect** property setting to Flat.


## Example

The following example sets the appearance of the text box **OrganizationName1** on the **Mailing List** form to Raised.


```vb
Forms("Mailing List").Controls("OrganizationName1").SpecialEffect = 1
```


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]