---
title: SharingItem.SaveAs method (Outlook)
keywords: vbaol11.chm630
f1_keywords:
- vbaol11.chm630
ms.prod: outlook
api_name:
- Outlook.SharingItem.SaveAs
ms.assetid: b18fae0e-b8be-9846-2f97-15b25f5f053b
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# SharingItem.SaveAs method (Outlook)

Saves the  **[SharingItem](Outlook.SharingItem.md)** to the specified path and in the format of the specified file type. If the file type is not specified, the MSG format (.msg) is used.


## Syntax

_expression_.**SaveAs** (_Path_, _Type_)

_expression_ A variable that represents a [SharingItem](Outlook.SharingItem.md) object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Path_|Required| **String**|The path in which to save the item.|
| _Type_|Optional| **Variant**|The file type to save. Can be one of the following  **OlSaveAsType** constants: **olHTML**, **olMSG**, **olRTF**, **olTemplate**, **olDoc**, **olTXT**, **olVCal**, **olVCard**, **olICal**, or **olMSGUnicode**.|

## Remarks

Also note that even though  **olDoc** is a valid **OlSaveAsType** constant, messages in HTML format cannot be saved in Document format, and the **olDoc** constant works only if Microsoft Word is set up as the default email editor.


## Example

This Visual Basic for Applications (VBA) example uses the  **SaveAs** method to save the currently open item as a text file in the Documents folder, using the subject as the file name. To run this example, make sure a mail item in plain text format is open in the active window.


```vb
Sub SaveAsTXT() 
 
 Dim myItem As Outlook.Inspector 
 
 Dim objItem As Object 
 
 
 
 Set myItem = Application.ActiveInspector 
 
 If Not TypeName(myItem) = "Nothing" Then 
 
 Set objItem = myItem.CurrentItem 
 
 strname = objItem.Subject 
 
 'Prompt the user for confirmation 
 
 Dim strPrompt As String 
 
 strPrompt = "Are you sure you want to save the item? " & _ 
 
 "If a file with the same name already exists, " & _ 
 
 "it will be overwritten with this copy of the file." 
 
 If MsgBox(strPrompt, vbYesNo + vbQuestion) = vbYes Then 
 
 objItem.SaveAs Environ("HOMEPATH") & "\My Documents\" & strname & ".txt", olTXT 
 
 End If 
 
 Else 
 
 MsgBox "There is no current active inspector." 
 
 End If 
 
End Sub
```


## See also


[SharingItem Object](Outlook.SharingItem.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]