---
title: Application.DDERequest method (Access)
keywords: vbaac10.chm12542
f1_keywords:
- vbaac10.chm12542
ms.prod: access
api_name:
- Access.Application.DDERequest
ms.assetid: c6f5f472-aeac-6de9-8133-bebfc5887eee
ms.date: 02/05/2019
ms.localizationpriority: medium
---


# Application.DDERequest method (Access)

You can use the **DDERequest** function over an open dynamic data exchange (DDE) channel to request an item of information from a DDE server application.


## Syntax

_expression_.**DDERequest** (_ChanNum_, _Item_)

_expression_ A variable that represents an **[Application](Access.Application.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _ChanNum_|Required|**Variant**|A channel number, the integer returned by the **[DDEInitiate](Access.Application.DDEInitiate.md)** function.|
| _Item_|Required|**String**|A string expression that's the name of a data item recognized by the application specified by the **DDEInitiate** function. Check the application's documentation for a list of possible items.|

## Return value

String


## Remarks

For example, if you have an open DDE channel between Microsoft Access and Microsoft Excel, you can use the **DDERequest** function to transfer text from an Excel spreadsheet to an Access database.

The _channum_ argument specifies the channel number of the desired DDE conversation, and the _item_ argument identifies which data should be retrieved from the server application. The value of the _item_ argument depends on the application and topic specified when the channel indicated by the _channum_ argument is opened. For example, the _item_ argument may be a range of cells in an Excel spreadsheet.

The **DDERequest** function returns a **Variant** as a string containing the requested information if the request was successful.

The data is requested in alphanumeric text format. Graphics or text in any other format can't be transferred.

If the _channum_ argument isn't an integer corresponding to an open channel, or if the data requested can't be transferred, a run-time error occurs.

If you need to manipulate another application's objects from Access, you may want to consider using Automation.



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]