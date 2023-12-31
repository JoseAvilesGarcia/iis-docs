---
title: SmoothStreamingMediaElement.SmoothStreamingSource Property (Microsoft.Web.Media.SmoothStreaming)
description: Describes the SmoothStreamingSource property and provides the property's syntax, property value, remarks, and version information.
TOCTitle: SmoothStreamingSource Property
ms:assetid: P:Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.SmoothStreamingSource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.smoothstreaming.smoothstreamingmediaelement.smoothstreamingsource(v=VS.90)
ms:contentKeyID: 23961153
ms.date: 05/02/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.SmoothStreamingSource
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.get_SmoothStreamingSource
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.set_SmoothStreamingSource
dev_langs:
- csharp
- jscript
- vb
- cpp
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.get_SmoothStreamingSource
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.set_SmoothStreamingSource
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.SmoothStreamingSource
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# SmoothStreamingSource Property

Gets or sets the URI of the Smooth Streaming source.

**Namespace:**  [Microsoft.Web.Media.SmoothStreaming](microsoft-web-media-smoothstreaming-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

  Public Property SmoothStreamingSource As Uri
'Usage

  Dim instance As SmoothStreamingMediaElement
Dim value As Uri

value = instance.SmoothStreamingSource

instance.SmoothStreamingSource = value
```

```csharp
  public Uri SmoothStreamingSource { get; set; }
```

```cpp
  public:
property Uri^ SmoothStreamingSource {
    Uri^ get ();
    void set (Uri^ value);
}
```

```jscript
  function get SmoothStreamingSource () : Uri
function set SmoothStreamingSource (value : Uri)
```

### Property Value

Type: [System.Uri](https://msdn.microsoft.com/library/txt7706a)  
The URI of the Smooth Streaming source.  

## Remarks

When you call [SetSource(Stream)](smoothstreamingmediaelement-setsource-method-microsoft-web-media-smoothstreaming_1.md) or assign the SmoothStreamingSource or [Source](smoothstreamingmediaelement-source-property-microsoft-web-media-smoothstreaming_1.md) properties, [Source](smoothstreamingmediaelement-source-property-microsoft-web-media-smoothstreaming_1.md) is reset to SmoothStreamingSource. However, SmoothStreamingSource is not cleared when reset to a progressive-downloading source.

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
