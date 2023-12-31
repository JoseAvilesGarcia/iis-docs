---
title: SmoothStreamingMediaElement.StartPosition Property (Microsoft.Web.Media.SmoothStreaming)
description: Describes the SmoothStreamingMediaElement.StartPosition property and provides the property's syntax, property value, and version information.
TOCTitle: StartPosition Property
ms:assetid: P:Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.StartPosition
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.smoothstreaming.smoothstreamingmediaelement.startposition(v=VS.95)
ms:contentKeyID: 46307854
ms.date: 05/31/2012
mtps_version: v=VS.95
f1_keywords:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.StartPosition
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.get_StartPosition
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.set_StartPosition
dev_langs:
- csharp
- jscript
- vb
- FSharp
- cpp
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.get_StartPosition
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.set_StartPosition
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.StartPosition
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# SmoothStreamingMediaElement.StartPosition Property

Gets or sets the start position of the current stream.

**Namespace:**  [Microsoft.Web.Media.SmoothStreaming](microsoft-web-media-smoothstreaming-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

Public Property StartPosition As TimeSpan
    Get
    Set
'Usage

Dim instance As SmoothStreamingMediaElement
Dim value As TimeSpan

value = instance.StartPosition

instance.StartPosition = value
```

```csharp
public TimeSpan StartPosition { get; set; }
```

```cpp
public:
property TimeSpan StartPosition {
    TimeSpan get ();
    void set (TimeSpan value);
}
```

``` fsharp
member StartPosition : TimeSpan with get, set
```

```jscript
function get StartPosition () : TimeSpan
function set StartPosition (value : TimeSpan)
```

### Property Value

Type: [System.TimeSpan](https://msdn.microsoft.com/library/269ew577\(v=vs.95\))  
The start position.

## Version Information

### Silverlight

Supported in: 5  

### Windows Phone

Supported in: Windows Phone OS 7.1, Windows Phone OS 7.0  

## See Also

### Reference

[SmoothStreamingMediaElement Class](smoothstreamingmediaelement-class-microsoft-web-media-smoothstreaming_1.md)

[Microsoft.Web.Media.SmoothStreaming Namespace](microsoft-web-media-smoothstreaming-namespace_1.md)
