---
title: TaskStatus.Message Property (Microsoft.Web.Media.TransformManager)
description: Learn about the TaskStatus.Message property, specifically learn details about its syntax and property value.
TOCTitle: Message Property
ms:assetid: P:Microsoft.Web.Media.TransformManager.TaskStatus.Message
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.transformmanager.taskstatus.message(v=VS.90)
ms:contentKeyID: 46408743
ms.date: 06/14/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.TransformManager.TaskStatus.get_Message
- Microsoft.Web.Media.TransformManager.TaskStatus.Message
dev_langs:
- csharp
- jscript
- vb
- FSharp
- cpp
api_location:
- Microsoft.Web.Media.TransformManager.Common.dll
api_name:
- Microsoft.Web.Media.TransformManager.TaskStatus.get_Message
- Microsoft.Web.Media.TransformManager.TaskStatus.Message
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# Message Property

**Namespace:**  [Microsoft.Web.Media.TransformManager](microsoft-web-media-transformmanager-namespace.md)  
**Assembly:**  Microsoft.Web.Media.TransformManager.Common (in Microsoft.Web.Media.TransformManager.Common.dll)

## Syntax

```vb
'Declaration

  Public ReadOnly Property Message As String
    Get
'Usage

  Dim instance As TaskStatus
Dim value As String

value = instance.Message
```

```csharp
  public string Message { get; }
```

```cpp
  public:
virtual property String^ Message {
    String^ get () sealed;
}
```

``` fsharp
  abstract Message : string
override Message : string
```

```jscript
  final function get Message () : String
```

### Property Value

Type: [System.String](https://msdn.microsoft.com/library/s1wwdcbf)  

### Implements

[ITaskStatus.Message](itaskstatus-message-property-microsoft-web-media-transformmanager.md)  

## See Also

### Reference

[TaskStatus Class](taskstatus-class-microsoft-web-media-transformmanager.md)

[Microsoft.Web.Media.TransformManager Namespace](microsoft-web-media-transformmanager-namespace.md)
