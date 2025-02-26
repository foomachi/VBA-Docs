---
title: PivotCell.PivotTable property (Excel)
keywords: vbaxl10.chm692074
f1_keywords:
- vbaxl10.chm692074
ms.prod: excel
api_name:
- Excel.PivotCell.PivotTable
ms.assetid: ac34eb5b-be2f-a58c-484b-d53cc82afa81
ms.date: 05/04/2019
ms.localizationpriority: medium
---


# PivotCell.PivotTable property (Excel)

Returns a **[PivotTable](Excel.PivotTable.md)** object that represents the PivotTable report associated with the PivotCell.


## Syntax

_expression_.**PivotTable**

_expression_ A variable that represents a **[PivotCell](Excel.PivotCell.md)** object.


## Example

This example sets the current page for the PivotTable report on Sheet1 to the page named Canada.

```vb
Set pvtTable = Worksheets("Sheet1").Range("A3").PivotTable 
pvtTable.PivotFields("Country").CurrentPage = "Canada"
```

<br/>

This example determines the PivotTable report associated with the Sales chart on the active worksheet, and then it sets the page named Oregon as the current page for the PivotTable report.

```vb
Set objPT = _ 
 ActiveSheet.Charts("Sales").PivotLayout.PivotTable 
objPT.PivotFields("State").CurrentPageName = "Oregon"
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]