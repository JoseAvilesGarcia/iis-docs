---
title: StreamInfo.AvailableTracks Property (Microsoft.Web.Media.SmoothStreaming)
description: Describes the StreamInfo.AvailableTracks property and provides the property's syntax, remarks, and version information.
TOCTitle: AvailableTracks Property
ms:assetid: P:Microsoft.Web.Media.SmoothStreaming.StreamInfo.AvailableTracks
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.smoothstreaming.streaminfo.availabletracks(v=VS.95)
ms:contentKeyID: 46307861
ms.date: 05/31/2012
mtps_version: v=VS.95
f1_keywords:
- Microsoft.Web.Media.SmoothStreaming.StreamInfo.AvailableTracks
- Microsoft.Web.Media.SmoothStreaming.StreamInfo.get_AvailableTracks
dev_langs:
- csharp
- jscript
- vb
- FSharp
- cpp
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.SmoothStreaming.StreamInfo.AvailableTracks
- Microsoft.Web.Media.SmoothStreaming.StreamInfo.get_AvailableTracks
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# StreamInfo.AvailableTracks Property

Gets the AvailableTracks property.

**Namespace:**  [Microsoft.Web.Media.SmoothStreaming](microsoft-web-media-smoothstreaming-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

Public ReadOnly Property AvailableTracks As IList(Of TrackInfo)
    Get
'Usage

Dim instance As StreamInfo
Dim value As IList(Of TrackInfo)

value = instance.AvailableTracks
```

```csharp
public IList<TrackInfo> AvailableTracks { get; }
```

```cpp
public:
property IList<TrackInfo^>^ AvailableTracks {
    IList<TrackInfo^>^ get ();
}
```

``` fsharp
member AvailableTracks : IList<TrackInfo>
```

```jscript
function get AvailableTracks () : IList<TrackInfo>
```

### Property Value

Type: [System.Collections.Generic.IList](https://msdn.microsoft.com/library/5y536ey6\(v=vs.95\))\<[TrackInfo](trackinfo-class-microsoft-web-media-smoothstreaming_1.md)\>  
A generic list of [TrackInfo](trackinfo-class-microsoft-web-media-smoothstreaming_1.md) objects.

## Remarks

For more information and an example that parses [StreamInfo](streaminfo-class-microsoft-web-media-smoothstreaming_1.md) objects, see [Timeline Markers and Events](timeline-markers-and-events.md) under the heading "Extract Timeline Events and Assign Markers."

## Version Information

### Silverlight

Supported in: 5  

### Windows Phone

Supported in: Windows Phone OS 7.1, Windows Phone OS 7.0  

## See Also

### Reference

[StreamInfo Class](streaminfo-class-microsoft-web-media-smoothstreaming_1.md)

[Microsoft.Web.Media.SmoothStreaming Namespace](microsoft-web-media-smoothstreaming-namespace_1.md)
