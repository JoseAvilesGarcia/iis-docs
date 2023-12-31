---
title: SmoothStreamingMediaElement.Attributes Property (Microsoft.Web.Media.SmoothStreaming)
TOCTitle: Attributes Property
description: "The SmoothStreamingMediaElement.Attributes property gets or sets the attributes dictionary. This article describes its syntax, examples, version information, and permissions."
ms:assetid: P:Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.Attributes
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.smoothstreaming.smoothstreamingmediaelement.attributes(v=VS.90)
ms:contentKeyID: 23961271
ms.date: 05/02/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.Attributes
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.get_Attributes
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.set_Attributes
dev_langs:
- csharp
- jscript
- vb
- cpp
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.Attributes
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.get_Attributes
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.set_Attributes
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# Attributes Property

Gets or sets the attributes dictionary.

**Namespace:**  [Microsoft.Web.Media.SmoothStreaming](microsoft-web-media-smoothstreaming-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

  Public Property Attributes As Dictionary(Of String, String)
'Usage

  Dim instance As SmoothStreamingMediaElement
Dim value As Dictionary(Of String, String)

value = instance.Attributes

instance.Attributes = value
```

```csharp
  public Dictionary<string, string> Attributes { get; set; }
```

```cpp
  public:
property Dictionary<String^, String^>^ Attributes {
    Dictionary<String^, String^>^ get ();
    void set (Dictionary<String^, String^>^ value);
}
```

```jscript
  function get Attributes () : Dictionary<String, String>
function set Attributes (value : Dictionary<String, String>)
```

### Property Value

Type: [System.Collections.Generic.Dictionary](https://msdn.microsoft.com/library/xfhwa508)\< (Of \< ( \<'[String](https://msdn.microsoft.com/library/s1wwdcbf), [String](https://msdn.microsoft.com/library/s1wwdcbf)\> ) \> ) \>  
A dictionary object that contains name/value pairs for the attributes.  

## Examples

The following example shows how to get attributes.

``` 
    if (streamInfo.Attributes["Name"] == "ClosedCaptions" ||
                            streamInfo.Attributes["Name"] == "MARKERS")
    {
        selectStreams.Add(streamInfo);
        segmentInfo.SelectStreamsAsync(selectStreams);

        foreach (TrackInfo trackInfo in streamInfo.SelectedTracks)
        {
            foreach (ChunkInfo chunk in streamInfo.ChunkList.ToList<ChunkInfo>())
            {
                IAsyncResult ar =
                    trackInfo.BeginGetChunk(
                    chunk.TimeStamp, new AsyncCallback(AddMarkers), streamInfo.UniqueId);
            }
        }
    }
```

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
