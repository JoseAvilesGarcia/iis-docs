---
title: SmoothStreamingMediaElement.Markers Property (Microsoft.Web.Media.SmoothStreaming)
description: Describes the Markers property and provides the property's namespace, assembly, syntax, property value, version information, and permissions.
TOCTitle: Markers Property
ms:assetid: P:Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.Markers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.smoothstreaming.smoothstreamingmediaelement.markers(v=VS.90)
ms:contentKeyID: 23961263
ms.date: 05/02/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.Markers
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.get_Markers
dev_langs:
- csharp
- jscript
- vb
- cpp
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.get_Markers
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.Markers
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# Markers Property

Gets the markers collection.

**Namespace:**  [Microsoft.Web.Media.SmoothStreaming](microsoft-web-media-smoothstreaming-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

  Public ReadOnly Property Markers As TimelineMarkerCollection
'Usage

  Dim instance As SmoothStreamingMediaElement
Dim value As TimelineMarkerCollection

value = instance.Markers
```

```csharp
  public TimelineMarkerCollection Markers { get; }
```

```cpp
  public:
property TimelineMarkerCollection^ Markers {
    TimelineMarkerCollection^ get ();
}
```

```jscript
  function get Markers () : TimelineMarkerCollection
```

### Property Value

Type: [System.Windows.Media.TimelineMarkerCollection](https://msdn.microsoft.com/library/cc190313)  
A collection of timeline markers.  

## Remarks

For more information, see [Timeline Markers and Events (IIS Smooth Streaming)](timeline-markers-and-events.md).

## Version Information

### Silverlight

Supported in: 4  

## Permissions

  - Full trust for the immediate caller. This member cannot be used by partially trusted code. For more information, see [Using Libraries from Partially Trusted Code](https://msdn.microsoft.com/library/8skskf63).

## See Also

### Reference

[SmoothStreamingMediaElement Class](smoothstreamingmediaelement-class-microsoft-web-media-smoothstreaming_1.md)

[Microsoft.Web.Media.SmoothStreaming Namespace](microsoft-web-media-smoothstreaming-namespace_1.md)
