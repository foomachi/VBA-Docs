---
title: Styles.StyleDeleteCanceled event (Visio)
keywords: vis_sdr.chm11519350
f1_keywords:
- vis_sdr.chm11519350
ms.prod: visio
api_name:
- Visio.Styles.StyleDeleteCanceled
ms.assetid: 809941a8-ef8d-0c7c-d9fd-e1806914389d
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Styles.StyleDeleteCanceled event (Visio)

Occurs after an event handler has returned  **True** (cancel) to a **QueryCancelStyleDelete** event.


## Syntax

_expression_.**StyleDeleteCanceled** (_Style_)

_expression_ A variable that represents a **[Styles](Visio.Styles.md)** object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Style_|Required| **[IVSTYLE]**|The style that was going to be deleted.|

## Remarks

If you are using Microsoft Visual Basic or Visual Basic for Applications (VBA), the syntax in this topic describes a common, efficient way to handle events.

If you want to create your own **Event** objects, use the **[Add](visio.eventlist.add.md)** or **[AddAdvise](visio.eventlist.addadvise.md)** method. 

To create an **Event** object that runs an add-on, use the **Add** method as it applies to the **EventList** collection. 

To create an **Event** object that receives notification, use the **AddAdvise** method. 

To find an event code for the event that you want to create, see [Event codes](../visio/Concepts/event-codesvisio.md).

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]