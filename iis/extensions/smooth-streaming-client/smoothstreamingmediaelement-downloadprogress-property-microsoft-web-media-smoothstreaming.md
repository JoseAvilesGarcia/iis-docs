---
title: SmoothStreamingMediaElement.DownloadProgress Property (Microsoft.Web.Media.SmoothStreaming)
description: This article contains syntax and version information for the DownloadProgress property, as well as links to reference materials. 
TOCTitle: DownloadProgress Property
ms:assetid: P:Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.DownloadProgress
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.smoothstreaming.smoothstreamingmediaelement.downloadprogress(v=VS.90)
ms:contentKeyID: 23961039
ms.date: 05/02/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.DownloadProgress
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.get_DownloadProgress
dev_langs:
- csharp
- jscript
- vb
- cpp
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.DownloadProgress
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.get_DownloadProgress
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# DownloadProgress Property

Gets or sets the download progress.

**Namespace:**  [Microsoft.Web.Media.SmoothStreaming](microsoft-web-media-smoothstreaming-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

  Public ReadOnly Property DownloadProgress As Double
'Usage

  Dim instance As SmoothStreamingMediaElement
Dim value As Double

value = instance.DownloadProgress
```

```csharp
  public double DownloadProgress { get; }
```

```cpp
  public:
property double DownloadProgress {
    double get ();
}
```

```jscript
  function get DownloadProgress () : double
```

### Property Value

Type: [System.Double](https://msdn.microsoft.com/library/643eft0t)  
AS value that indicates the percentage progress of the download.  

## Version Information

### Silverlight

Supported in: 4  

### Silverlight for Windows Phone

Supported in: Windows Phone OS 7.0  

## Permissions

  - Full trust for the immediate caller. This member cannot be used by partially trusted code. For more information, see [Using Libraries from Partially Trusted Code](https://msdn.microsoft.com/library/8skskf63).

## See Also

### Reference

[SmoothStreamingMediaElement Class](smoothstreamingmediaelement-class-microsoft-web-media-smoothstreaming_1.md)

[Microsoft.Web.Media.SmoothStreaming Namespace](microsoft-web-media-smoothstreaming-namespace_1.md)
