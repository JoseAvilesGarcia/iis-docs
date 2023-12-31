---
title: IisNamespaces.MediaServices Property (Microsoft.Web.Media.TransformManager)
description: Describes the IisNamespaces.MediaServices Property and details its namespace, assembly, syntax, and property value. 
TOCTitle: MediaServices Property
ms:assetid: P:Microsoft.Web.Media.TransformManager.IisNamespaces.MediaServices
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.transformmanager.iisnamespaces.mediaservices(v=VS.90)
ms:contentKeyID: 35520700
ms.date: 06/14/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.TransformManager.IisNamespaces.MediaServices
- Microsoft.Web.Media.TransformManager.IisNamespaces.get_MediaServices
dev_langs:
- csharp
- jscript
- vb
- FSharp
- cpp
api_location:
- Microsoft.Web.Media.TransformManager.Sdk.dll
api_name:
- Microsoft.Web.Media.TransformManager.IisNamespaces.get_MediaServices
- Microsoft.Web.Media.TransformManager.IisNamespaces.MediaServices
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# MediaServices Property

Gets the URI of a media services schema document.

**Namespace:**  [Microsoft.Web.Media.TransformManager](microsoft-web-media-transformmanager-namespace.md)  
**Assembly:**  Microsoft.Web.Media.TransformManager.Sdk (in Microsoft.Web.Media.TransformManager.Sdk.dll)

## Syntax

```vb
'Declaration

  Public Shared ReadOnly Property MediaServices As XNamespace
    Get
'Usage

  Dim value As XNamespace

value = IisNamespaces.MediaServices
```

```csharp
  public static XNamespace MediaServices { get; }
```

```cpp
  public:
static property XNamespace^ MediaServices {
    XNamespace^ get ();
}
```

``` fsharp
  static member MediaServices : XNamespace
```

```jscript
  static function get MediaServices () : XNamespace
```

### Property Value

Type: [System.Xml.Linq.XNamespace](https://msdn.microsoft.com/library/bb291898)  
The XML namespace value "http://schemas.microsoft.com/iis/media/v4/TM\#".  

## See Also

### Reference

[IisNamespaces Class](iisnamespaces-class-microsoft-web-media-transformmanager.md)

[Microsoft.Web.Media.TransformManager Namespace](microsoft-web-media-transformmanager-namespace.md)
