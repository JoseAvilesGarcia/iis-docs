---
title: TrackInfo.EndGetChunk Method  (Microsoft.Web.Media.SmoothStreaming)
description: This article contains syntax and version information for the TrackInfo.EndGetChunk method. There are also links to reference materials.
TOCTitle: EndGetChunk Method
ms:assetid: M:Microsoft.Web.Media.SmoothStreaming.TrackInfo.EndGetChunk(System.IAsyncResult)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.smoothstreaming.trackinfo.endgetchunk(v=VS.95)
ms:contentKeyID: 46307700
ms.date: 05/31/2012
mtps_version: v=VS.95
f1_keywords:
- Microsoft.Web.Media.SmoothStreaming.TrackInfo.EndGetChunk
dev_langs:
- csharp
- jscript
- vb
- FSharp
- "cpp"
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.SmoothStreaming.TrackInfo.EndGetChunk
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# TrackInfo.EndGetChunk Method

Method to complete the action of [BeginGetChunk](trackinfo-begingetchunk-method-microsoft-web-media-smoothstreaming_1.md).

**Namespace:**  [Microsoft.Web.Media.SmoothStreaming](microsoft-web-media-smoothstreaming-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

Public Overridable Function EndGetChunk ( _
    ar As IAsyncResult _
) As ChunkResult
'Usage

Dim instance As TrackInfo
Dim ar As IAsyncResult
Dim returnValue As ChunkResult

returnValue = instance.EndGetChunk(ar)
```

```csharp
public virtual ChunkResult EndGetChunk(
    IAsyncResult ar
)
```

```cpp
public:
virtual ChunkResult^ EndGetChunk(
    IAsyncResult^ ar
)
```

``` fsharp
abstract EndGetChunk : 
        ar:IAsyncResult -> ChunkResult 
override EndGetChunk : 
        ar:IAsyncResult -> ChunkResult 
```

```jscript
public function EndGetChunk(
    ar : IAsyncResult
) : ChunkResult
```

### Parameters

  - ar  
    Type: [System.IAsyncResult](https://msdn.microsoft.com/library/ft8a6455\(v=vs.95\))  
    An [IAsyncResult](https://msdn.microsoft.com/library/ft8a6455\(v=vs.95\)) object from [BeginGetChunk](trackinfo-begingetchunk-method-microsoft-web-media-smoothstreaming_1.md).

### Return Value

Type: [Microsoft.Web.Media.SmoothStreaming.ChunkResult](chunkresult-class-microsoft-web-media-smoothstreaming_1.md)  
A [ChunkResult](chunkresult-class-microsoft-web-media-smoothstreaming_1.md) object.

## Examples

The following example loops through tracks and calls the EndGetChunk(IAsyncResult) method on each track. This method completes an asynchronous process started by [BeginGetChunk(TimeSpan, AsyncCallback, Object)](trackinfo-begingetchunk-method-microsoft-web-media-smoothstreaming_1.md). The [ChunkResult](chunkresult-class-microsoft-web-media-smoothstreaming_1.md) indicates success or failure. If the method succeeds, the [ChunkResult](chunkresult-class-microsoft-web-media-smoothstreaming_1.md) contains the Base64-encoded data. For the complete example and more information, see [Timeline Markers and Events](timeline-markers-and-events.md).

``` 
    foreach (TrackInfo trackInfo in streamInfo.SelectedTracks)
    {
        ChunkResult chunkResult = trackInfo.EndGetChunk(argAR);

        if (chunkResult.Result == ChunkResult.ChunkResultState.Succeeded)
        {
            System.Text.Encoding enc = System.Text.Encoding.UTF8;
            int length = (int)chunkResult.ChunkData.Length;
            byte[] rawData = new byte[length];
            chunkResult.ChunkData.Read(rawData, 0, length);
            String text = enc.GetString(rawData, 0, rawData.Length);
            TimelineMarker newMarker = new TimelineMarker();
            newMarker.Text = text;
            newMarker.Time = chunkResult.Timestamp;

            SmoothPlayer.Markers.Add(newMarker);
        }
    }
```

## Version Information

### Silverlight

Supported in: 5  

## See Also

### Reference

[TrackInfo Class](trackinfo-class-microsoft-web-media-smoothstreaming_1.md)

[Microsoft.Web.Media.SmoothStreaming Namespace](microsoft-web-media-smoothstreaming-namespace_1.md)
