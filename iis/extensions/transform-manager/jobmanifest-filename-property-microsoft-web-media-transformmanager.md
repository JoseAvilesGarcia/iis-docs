---
title: JobManifest.FileName Property (Microsoft.Web.Media.TransformManager)
TOCTitle: FileName Property
description: This article contains syntax, property value, and reference information for the JobManifest.FileName property.
ms:assetid: P:Microsoft.Web.Media.TransformManager.JobManifest.FileName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.transformmanager.jobmanifest.filename(v=VS.90)
ms:contentKeyID: 35520861
ms.date: 06/14/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.TransformManager.JobManifest.set_FileName
- Microsoft.Web.Media.TransformManager.JobManifest.FileName
- Microsoft.Web.Media.TransformManager.JobManifest.get_FileName
dev_langs:
- csharp
- jscript
- vb
- FSharp
- cpp
api_location:
- Microsoft.Web.Media.TransformManager.Common.dll
api_name:
- Microsoft.Web.Media.TransformManager.JobManifest.FileName
- Microsoft.Web.Media.TransformManager.JobManifest.get_FileName
- Microsoft.Web.Media.TransformManager.JobManifest.set_FileName
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# FileName Property

Gets or sets the file name of the manifest.

**Namespace:**  [Microsoft.Web.Media.TransformManager](microsoft-web-media-transformmanager-namespace.md)  
**Assembly:**  Microsoft.Web.Media.TransformManager.Common (in Microsoft.Web.Media.TransformManager.Common.dll)

## Syntax

```vb
'Declaration

  Public Property FileName As String
    Get
    Set
'Usage

  Dim instance As JobManifest
Dim value As String

value = instance.FileName

instance.FileName = value
```

```csharp
  public string FileName { get; set; }
```

```cpp
  public:
property String^ FileName {
    String^ get ();
    void set (String^ value);
}
```

``` fsharp
  member FileName : string with get, set
```

```jscript
  function get FileName () : String
function set FileName (value : String)
```

### Property Value

Type: [System.String](https://msdn.microsoft.com/library/s1wwdcbf)  
The file name of the manifest.  

## See Also

### Reference

[JobManifest Class](jobmanifest-class-microsoft-web-media-transformmanager.md)

[Microsoft.Web.Media.TransformManager Namespace](microsoft-web-media-transformmanager-namespace.md)
