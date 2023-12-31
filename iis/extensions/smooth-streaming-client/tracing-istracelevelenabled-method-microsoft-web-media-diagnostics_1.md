---
title: Tracing.IsTraceLevelEnabled Method  (Microsoft.Web.Media.Diagnostics)
description: This article contains syntax and version information for the Tracing.IsTraceLevelEnabled method, with links to reference materials.
TOCTitle: IsTraceLevelEnabled Method
ms:assetid: M:Microsoft.Web.Media.Diagnostics.Tracing.IsTraceLevelEnabled(Microsoft.Web.Media.Diagnostics.TraceLevel)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.diagnostics.tracing.istracelevelenabled(v=VS.95)
ms:contentKeyID: 46307622
ms.date: 05/31/2012
mtps_version: v=VS.95
f1_keywords:
- Microsoft.Web.Media.Diagnostics.Tracing.IsTraceLevelEnabled
dev_langs:
- csharp
- jscript
- vb
- FSharp
- "cpp"
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.Diagnostics.Tracing.IsTraceLevelEnabled
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# Tracing.IsTraceLevelEnabled Method

Returns a Boolean value that indicates whether the specified TraceLevel severity is enabled.

**Namespace:**  [Microsoft.Web.Media.Diagnostics](microsoft-web-media-diagnostics-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

Public Shared Function IsTraceLevelEnabled ( _
    traceLevel As TraceLevel _
) As Boolean
'Usage

Dim traceLevel As TraceLevel
Dim returnValue As Boolean

returnValue = Tracing.IsTraceLevelEnabled(traceLevel)
```

```csharp
public static bool IsTraceLevelEnabled(
    TraceLevel traceLevel
)
```

```cpp
public:
static bool IsTraceLevelEnabled(
    TraceLevel traceLevel
)
```

``` fsharp
static member IsTraceLevelEnabled : 
        traceLevel:TraceLevel -> bool 
```

```jscript
public static function IsTraceLevelEnabled(
    traceLevel : TraceLevel
) : boolean
```

### Parameters

  - traceLevel  
    Type: [Microsoft.Web.Media.Diagnostics.TraceLevel](tracelevel-enumeration-microsoft-web-media-diagnostics_1.md)  
    A [TraceLevel](tracelevel-enumeration-microsoft-web-media-diagnostics_1.md) enumeration object.

### Return Value

Type: [System.Boolean](https://msdn.microsoft.com/library/a28wyd50\(v=vs.95\))  
A Boolean value, true if the specified TraceLevel is enabled, otherwise false.

## Version Information

### Silverlight

Supported in: 5  

### Windows Phone

Supported in: Windows Phone OS 7.1, Windows Phone OS 7.0  

## See Also

### Reference

[Tracing Class](tracing-class-microsoft-web-media-diagnostics_1.md)

[Microsoft.Web.Media.Diagnostics Namespace](microsoft-web-media-diagnostics-namespace_1.md)
