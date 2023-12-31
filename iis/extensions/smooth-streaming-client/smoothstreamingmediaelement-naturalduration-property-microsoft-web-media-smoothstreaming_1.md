---
title: SmoothStreamingMediaElement.NaturalDuration Property (Microsoft.Web.Media.SmoothStreaming)
description: Describes the syntax for the SmoothStreamingMediaElement.NaturalDuration property and gets the duration of the current stream when it plays to the end.
TOCTitle: NaturalDuration Property
ms:assetid: P:Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.NaturalDuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.smoothstreaming.smoothstreamingmediaelement.naturalduration(v=VS.95)
ms:contentKeyID: 46307838
ms.date: 05/31/2012
mtps_version: v=VS.95
f1_keywords:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.NaturalDuration
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.get_NaturalDuration
dev_langs:
- csharp
- jscript
- vb
- FSharp
- cpp
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.get_NaturalDuration
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.NaturalDuration
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# SmoothStreamingMediaElement.NaturalDuration Property

Gets the duration of the current stream when it plays to the end.

**Namespace:**  [Microsoft.Web.Media.SmoothStreaming](microsoft-web-media-smoothstreaming-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

Public ReadOnly Property NaturalDuration As Duration
    Get
'Usage

Dim instance As SmoothStreamingMediaElement
Dim value As Duration

value = instance.NaturalDuration
```

```csharp
public Duration NaturalDuration { get; }
```

```cpp
public:
property Duration NaturalDuration {
    Duration get ();
}
```

``` fsharp
member NaturalDuration : Duration
```

```jscript
function get NaturalDuration () : Duration
```

### Property Value

Type: [System.Windows.Duration](https://msdn.microsoft.com/library/ms602372\(v=vs.95\))  
The duration of the stream.

## Version Information

### Silverlight

Supported in: 5  

### Windows Phone

Supported in: Windows Phone OS 7.1, Windows Phone OS 7.0  

## See Also

### Reference

[SmoothStreamingMediaElement Class](smoothstreamingmediaelement-class-microsoft-web-media-smoothstreaming_1.md)

[Microsoft.Web.Media.SmoothStreaming Namespace](microsoft-web-media-smoothstreaming-namespace_1.md)
