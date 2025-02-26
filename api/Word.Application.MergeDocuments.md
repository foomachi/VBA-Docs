---
title: Application.MergeDocuments method (Word)
keywords: vbawd10.chm158335447
f1_keywords:
- vbawd10.chm158335447
ms.prod: word
api_name:
- Word.Application.MergeDocuments
ms.assetid: 445fe4df-a41a-6be0-f646-d310c71ec25e
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Application.MergeDocuments method (Word)

Compares two documents and returns a  **Document** object that represents the document that contains the differences between the two documents, marked using tracked changes.


## Syntax

_expression_. `MergeDocuments`( `_OriginalDocument_` , `_RevisedDocument_` , `_Destination_` , `_Granularity_` , `_CompareFormatting_` , `_CompareCaseChanges_` , `_CompareWhitespace_` , `_CompareTables_` , `_CompareHeaders_` , `_CompareFootnotes_` , `_CompareTextboxes_` , `_CompareFields_` , `_CompareComments_` , `_OriginalAuthor_` , `_RevisedAuthor_` , `_FormatFrom_` )

 _expression_ An expression that returns an **[Application](Word.Application.md)** object. 


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _OriginalDocument_|Required| **Document**|Specifies the path and file name of the original document.|
| _RevisedDocument_|Required| **Document**|Specifies the path and file name of the revised document to which to compare the original document.|
| _Destination_|Optional| **[WdCompareDestination](Word.WdCompareDestination.md)**|Specifies whether to create a new file or whether to mark the differences between the two documents in the original document or in the revised document. Default value is **wdCompareDestinationNew**.|
| _Granularity_|Optional| **[WdGranularity](Word.WdGranularity.md)**|Specifies whether changes are tracked by character or by word. Default value is **wdGranularityWordLevel**.|
| _CompareFormatting_|Optional| **Boolean**|Specifies whether to mark differences in formatting between the two documents. Default value is **True**.|
| _CompareCaseChanges_|Optional| **Boolean**|Specifies whether to mark differences in case between the two documents. Default value is **True**.|
| _CompareWhitespace_|Optional| **Boolean**|Specifies whether to mark differences in white space, such as paragraphs or spaces, between the two documents. Default value is **True**.|
| _CompareTables_|Optional| **Boolean**|Specifies whether to compare the differences in data contained in tables between the two documents. Default value is **True**.|
| _CompareHeaders_|Optional| **Boolean**|Specifies whether to compare differences in headers and footers between the two documents. Default value is **True**.|
| _CompareFootnotes_|Optional| **Boolean**|Specifies whether to compare differences in footnotes and endnotes between the two documents. Default value is **True**.|
| _CompareTextboxes_|Optional| **Boolean**|Specifies whether to compare differences in the data contained within text boxes between the two documents. Default value is **True**.|
| _CompareFields_|Optional| **Boolean**|Specifies whether to compare differences in fields between the two documents. Default value is **True**.|
| _CompareComments_|Optional| **Boolean**|Specifies whether to compare differences in comments between the two documents. Default value is **True**.|
| _OriginalAuthor_|Optional| **String**|Specifies the name of the author of the original document.|
| _RevisedAuthor_|Optional| **String**|Specifies the name of the person to use for unattributed changes after merging two documents.|
| _FormatFrom_|Optional| **WdMergeFormatFrom**|Specifies the document from which to retain formatting.|

## Return value

Document


## See also


[Application Object](Word.Application.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]