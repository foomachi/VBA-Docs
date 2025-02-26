---
title: ObjectFrame.ColumnHeads property (Access)
keywords: vbaac10.chm11578
f1_keywords:
- vbaac10.chm11578
ms.prod: access
api_name:
- Access.ObjectFrame.ColumnHeads
ms.assetid: f318f924-2629-8a7a-90b0-3ab386e50a22
ms.date: 03/01/2019
ms.localizationpriority: medium
---


# ObjectFrame.ColumnHeads property (Access)

You can use the **ColumnHeads** property to display a single row of column headings for list boxes, combo boxes, and OLE objects that accept column headings. You can also use this property to create a label for each entry in a chart control. What is actually displayed as the first-row column heading depends on the object's **RowSourceType** property setting. Read/write **Boolean**.


## Syntax

_expression_.**ColumnHeads**

_expression_ A variable that represents an **[ObjectFrame](Access.ObjectFrame.md)** object.


## Remarks

The **ColumnHeads** property uses the following settings.

|Setting|Visual Basic|Description|
|:-----|:-----|:-----|
|Yes|**True**|Column headings are enabled and either field captions, field names, or the first row of data items are used as column headings or chart labels.|
|No|**False**|(Default) Column headings are not enabled.|

For table fields, you can set this property on the **Lookup** tab of the Field Properties section of table Design view for fields with the **DisplayControl** property set to Combo Box or List Box.

The **RowSourceType** property specifies whether field names or the first row of data items are used to create column headings. If the **RowSourceType** property is set to Table/Query, the field names are used as column headings. If the field has a caption, the caption is displayed. For example, if a list box has three columns (the **ColumnCount** property is set to 3) and the **RowSourceType** property is set to Table/Query, the first three field names (or captions) are used as headings.

If the **RowSourceType** property is set to Value List, the first row of data items entered in the value list (as the setting of the **RowSource** property) will be column headings. For example, if a list box has three columns and the **RowSourceType** property is set to Value List, the first three items in the **RowSource** property setting are used as column headings.

If you can't select the first row of a list box or combo box in Form view, check to see if the **ColumnHeads** property is set to Yes.

Headings in combo boxes appear only when displaying the list in the control.




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]