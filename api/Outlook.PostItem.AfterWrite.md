---
title: PostItem.AfterWrite event (Outlook)
ms.prod: outlook
api_name:
- Outlook.PostItem.AfterWrite
ms.assetid: e1e31a7b-951c-d2e7-ad2c-b1a0ada0df6a
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# PostItem.AfterWrite event (Outlook)

Occurs after Microsoft Outlook has saved the item.


## Syntax

_expression_. `AfterWrite`

_expression_ A variable that represents a [PostItem](Outlook.PostItem.md) object.


## Remarks

The **AfterWrite** event occurs after the **[Write](Outlook.PostItem.Write.md)** event. This event is not cancelable. To determine when the item is unloaded from memory, use the **[Unload](Outlook.PostItem.Unload.md)** event.

The **AfterWrite** event corresponds to the Exchange Client Extensions (ECE) event **IExchExtMessageEvents::OnWriteComplete**.

Only the following members of the item object can be accessed in the  **AfterWrite** event:


-  **[Class](Outlook.PostItem.Class.md)**
    
-  **[MessageClass](Outlook.PostItem.MessageClass.md)**
    
-  **MAPIOBJECT**
    
The **MAPIOBJECT** property is a hidden property in the Outlook object model. This property provides access to the underlying MAPI **[IMessage](https://msdn.microsoft.com/library/cc842097%28office.14%29.aspx)** object, and can be invoked only via the **[IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)** interface. The property is accessible to programs written in languages such as C or C++ that support **IUnknown**. **MAPIOBJECT** is not available through the **[IDispatch](https://msdn.microsoft.com/library/ms221608.aspx)** interface. Development languages such as Visual Basic for Applications (VBA), Visual C#, and Visual Basic support the **IDispatch** interface and not **IUnknown**, and therefore, they cannot access **MAPIOBJECT**. If other properties or methods of the parent item are accessed in this event, Outlook raises an error.

The object obtained from the  **MAPIOBJECT** property in this event must contain all the changes persisted by Outlook. The implementer can call the **[SaveChanges](https://msdn.microsoft.com/library/cc842181%28office.14%29.aspx)** method on the **IMessage** object to persist changes to the underlying **IMessage** object represented by **MAPIOBJECT**, and Outlook will not revert those changes.

Implementers must release the object obtained from the  **MAPIOBJECT** property in the event before the event completes. Attempting to use that object outside the context of the event is unsupported and will lead to unpredictable behavior.


## See also


[PostItem Object](Outlook.PostItem.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]