---
title: SmoothStreamingMediaElement.CurrentState Property (Microsoft.Web.Media.SmoothStreaming)
description: Describes the CurrentState property and provides the property's syntax, property value, remarks, version information, and permissions.
TOCTitle: CurrentState Property
ms:assetid: P:Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.CurrentState
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.smoothstreaming.smoothstreamingmediaelement.currentstate(v=VS.90)
ms:contentKeyID: 23961227
ms.date: 05/02/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.CurrentState
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.get_CurrentState
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.set_CurrentState
dev_langs:
- csharp
- jscript
- vb
- cpp
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.CurrentState
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.get_CurrentState
- Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElement.set_CurrentState
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# CurrentState Property

Gets or sets the current state of playback.

**Namespace:**  [Microsoft.Web.Media.SmoothStreaming](microsoft-web-media-smoothstreaming-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

  Public Property CurrentState As SmoothStreamingMediaElementState
'Usage

  Dim instance As SmoothStreamingMediaElement
Dim value As SmoothStreamingMediaElementState

value = instance.CurrentState
```

```csharp
  public SmoothStreamingMediaElementState CurrentState { get; internal set; }
```

```cpp
  public:
property SmoothStreamingMediaElementState CurrentState {
    SmoothStreamingMediaElementState get ();
    internal: void set (SmoothStreamingMediaElementState value);
}
```

```jscript
  function get CurrentState () : SmoothStreamingMediaElementState
internal function set CurrentState (value : SmoothStreamingMediaElementState)
```

### Property Value

Type: [Microsoft.Web.Media.SmoothStreaming.SmoothStreamingMediaElementState](smoothstreamingmediaelementstate-enumeration-microsoft-web-media-smoothstreaming_1.md)  
A state object.  

## Remarks

State does not change to Stopped when the manifest/license manager URL is invalid; instead, it remains in Opening state.

For more information and for examples, see [IIS Smooth Streaming Client 1.5](microsoft-smooth-streaming-client-2-0.md).

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
