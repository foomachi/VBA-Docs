---
title: Range.Column property (Excel)
keywords: vbaxl10.chm144099
f1_keywords:
- vbaxl10.chm144099
ms.prod: excel
api_name:
- Excel.Range.Column
ms.assetid: 4f540fae-fc9f-30de-5d71-f6496b78930b
ms.date: 05/10/2019
ms.localizationpriority: medium
---


# Range.Column property (Excel)

Returns the number of the first column in the first area in the specified range. Read-only **Long**.


## Syntax

_expression_.**Column**

_expression_ A variable that represents a **[Range](excel.range(object).md)** object.


## Remarks

Column A returns 1, column B returns 2, and so on.

To return the number of the last column in the range, use the following expression.

`myRange.Columns(myRange.Columns.Count).Column`


## Example

This example sets the column width of every other column on Sheet1 to 4 points.

```vb
For Each col In Worksheets("Sheet1").Columns 
    If col.Column Mod 2 = 0 Then 
        col.ColumnWidth = 4 
    End If 
Next col
```

<br/>

This example deletes the empty columns from a selected range.

```vb
Sub Delete_Empty_Columns()
    'The range from which to delete the columns.
    Dim rnSelection As Range
    
    'Column and count variables used in the deletion process.
    Dim lnLastColumn As Long
    Dim lnColumnCount As Long
    Dim lnDeletedColumns As Long
    
    lnDeletedColumns = 0
    
    'Confirm that a range is selected, and that the range is contiguous.
    If TypeName(Selection) = "Range" Then
        If Selection.Areas.Count = 1 Then
            
            'Initialize the range to what the user has selected, and initialize the count for the upcoming FOR loop.
            Set rnSelection = Application.Selection
            lnLastColumn = rnSelection.Columns.Count
        
            'Start at the far-right column and work left: if the column is empty then
            'delete the column and increment the deleted column count.
            For lnColumnCount = lnLastColumn To 1 Step -1
                If Application.CountA(rnSelection.Columns(lnColumnCount)) = 0 Then
                    rnSelection.Columns(lnColumnCount).Delete
                    lnDeletedColumns = lnDeletedColumns + 1
                End If
            Next lnColumnCount
    
            rnSelection.Resize(lnLastColumn - lnDeletedColumns).Select
        Else
            MsgBox "Please select only one area.", vbInformation
        End If
    Else
        MsgBox "Please select a range.", vbInformation
    End If
    
    'Turn screen updating back on.
    Application.ScreenUpdating = True

End Sub
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
