---
title: CacheRequest.ReadFrom Method  (Microsoft.Web.Media.SmoothStreaming)
description: This article contains syntax, permissions, and version information for the CacheRequest.ReadFrom method.
TOCTitle: ReadFrom Method
ms:assetid: M:Microsoft.Web.Media.SmoothStreaming.CacheRequest.ReadFrom(System.IO.Stream)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.smoothstreaming.cacherequest.readfrom(v=VS.90)
ms:contentKeyID: 31469179
ms.date: 05/02/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.SmoothStreaming.CacheRequest.ReadFrom
dev_langs:
- csharp
- jscript
- vb
- cpp
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.SmoothStreaming.CacheRequest.ReadFrom
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# ReadFrom Method

Reads the request from a [Stream](https://msdn.microsoft.com/library/8f86tw9e) object. There is no default implementation for this method. Calling the method without implementing an override will result in a [NotSupportedException](https://msdn.microsoft.com/library/8a7a4e64).

**Namespace:**  [Microsoft.Web.Media.SmoothStreaming](microsoft-web-media-smoothstreaming-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

  Public Overridable Sub ReadFrom ( _
    stream As Stream _
)
'Usage

  Dim instance As CacheRequest
Dim stream As Stream

instance.ReadFrom(stream)
```

```csharp
  public virtual void ReadFrom(
    Stream stream
)
```

```cpp
  public:
virtual void ReadFrom(
    Stream^ stream
)
```

```jscript
  public function ReadFrom(
    stream : Stream
)
```

### Parameters

  - stream  
    Type: [System.IO.Stream](https://msdn.microsoft.com/library/8f86tw9e)  
    A [Stream](https://msdn.microsoft.com/library/8f86tw9e) object.  

## Version Information

### Silverlight

Supported in: 4  

### Silverlight for Windows Phone

Supported in: Windows Phone OS 7.0  

## Permissions

  - Full trust for the immediate caller. This member cannot be used by partially trusted code. For more information, see [Using Libraries from Partially Trusted Code](https://msdn.microsoft.com/library/8skskf63).

## See Also

### Reference

[CacheRequest Class](cacherequest-class-microsoft-web-media-smoothstreaming_1.md)

[Microsoft.Web.Media.SmoothStreaming Namespace](microsoft-web-media-smoothstreaming-namespace_1.md)
