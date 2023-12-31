---
title: SmoothStreamingMediaElement.ManifestMergeHandler Delegate (Microsoft.Web.Media.SmoothStreaming)
TOCTitle: SmoothStreamingMediaElement.ManifestMergeHandler Delegate
description: Describes the SmoothStreamingMediaElement.ManifestMergeHandler Delegate and provides the field's namespace, assembly, syntax, and version information.
ms:assetid: T:Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.ManifestMergeHandler
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.smoothstreaming.smoothstreamingmediaelement.manifestmergehandler(v=VS.95)
ms:contentKeyID: 46307949
ms.date: 05/31/2012
mtps_version: v=VS.95
f1_keywords:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.ManifestMergeHandler
dev_langs:
- csharp
- jscript
- vb
- FSharp
- cpp
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.SmoothStreaming.ManifestMergeHandler
- Microsoft.Web.Media.SmoothStreaming.ManifestMergeHandler..ctor
- Microsoft.Web.Media.SmoothStreaming.ManifestMergeHandler.BeginInvoke
- Microsoft.Web.Media.SmoothStreaming.ManifestMergeHandler.EndInvoke
- Microsoft.Web.Media.SmoothStreaming.ManifestMergeHandler.Invoke
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# SmoothStreamingMediaElement.ManifestMergeHandler Delegate

Delegate method to merge data from more than one manifest.

**Namespace:**  [Microsoft.Web.Media.SmoothStreaming](microsoft-web-media-smoothstreaming-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

Public Delegate Sub ManifestMergeHandler ( _
    ssme As SmoothStreamingMediaElement _
)
'Usage

Dim instance As New ManifestMergeHandler(AddressOf HandlerMethod)
```

```csharp
public delegate void ManifestMergeHandler(
    SmoothStreamingMediaElement ssme
)
```

```cpp
public delegate void ManifestMergeHandler(
    SmoothStreamingMediaElement^ ssme
)
```

``` fsharp
type ManifestMergeHandler = 
    delegate of 
        ssme:SmoothStreamingMediaElement -> unit
```

```jscript
JScript supports the use of delegates, but not the declaration of new ones.
```

### Parameters

  - ssme  
    Type: [Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement](smoothstreamingmediaelement-class-microsoft-web-media-smoothstreaming_1.md)  
    A [SmoothStreamingMediaElement](smoothstreamingmediaelement-class-microsoft-web-media-smoothstreaming_1.md) object.

## Version Information

### Silverlight

Supported in: 5  

## See Also

### Reference

[Microsoft.Web.Media.SmoothStreaming Namespace](microsoft-web-media-smoothstreaming-namespace_1.md)
