---
title: Tracing.DisableTraceDestination Method (Microsoft.Web.Media.Diagnostics)
description: "This article shares the syntax and parameters of the DisableTraceDestination Method, which disables the trace destination that is specified by the destination parameter."
TOCTitle: DisableTraceDestination Method
ms:assetid: M:Microsoft.Web.Media.Diagnostics.Tracing.DisableTraceDestination(Microsoft.Web.Media.Diagnostics.TraceDestination)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.diagnostics.tracing.disabletracedestination(v=VS.90)
ms:contentKeyID: 23961061
ms.date: 05/02/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.Diagnostics.Tracing.DisableTraceDestination
dev_langs:
- csharp
- jscript
- vb
- "cpp"
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.Diagnostics.Tracing.DisableTraceDestination
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# DisableTraceDestination Method

Disables the trace destination that is specified by the destination parameter.

**Namespace:**  [Microsoft.Web.Media.Diagnostics](microsoft-web-media-diagnostics-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

  Public Shared Sub DisableTraceDestination ( _
    destination As TraceDestination _
)
'Usage

  Dim destination As TraceDestination

Tracing.DisableTraceDestination(destination)
```

```csharp
  public static void DisableTraceDestination(
    TraceDestination destination
)
```

```cpp
  public:
static void DisableTraceDestination(
    TraceDestination destination
)
```

```jscript
  public static function DisableTraceDestination(
    destination : TraceDestination
)
```

### Parameters

  - destination  
    Type: [Microsoft.Web.Media.Diagnostics.TraceDestination](tracedestination-enumeration-microsoft-web-media-diagnostics_1.md)  
    A [TraceDestination](tracedestination-enumeration-microsoft-web-media-diagnostics_1.md) enumeration object.  

## Version Information

### Silverlight

Supported in: 4  

### Silverlight for Windows Phone

Supported in: Windows Phone OS 7.0  

## Permissions

  - Full trust for the immediate caller. This member cannot be used by partially trusted code. For more information, see [Using Libraries from Partially Trusted Code](https://msdn.microsoft.com/library/8skskf63).

## See Also

### Reference

[Tracing Class](tracing-class-microsoft-web-media-diagnostics_1.md)

[Microsoft.Web.Media.Diagnostics Namespace](microsoft-web-media-diagnostics-namespace_1.md)
