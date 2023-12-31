---
title: Tracing.TraceFunctionEntry Method (String, String, String, TraceArea) (Microsoft.Web.Media.Diagnostics)
TOCTitle: TraceFunctionEntry Method (String, String, String, TraceArea)
description: Records the entry into a function as specified by the parameters.
ms:assetid: M:Microsoft.Web.Media.Diagnostics.Tracing.TraceFunctionEntry(System.String,System.String,System.String,Microsoft.Web.Media.Diagnostics.TraceArea)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.diagnostics.tracing.tracefunctionentry(v=VS.90)
ms:contentKeyID: 23961133
ms.date: 05/02/2012
mtps_version: v=VS.90
dev_langs:
- vb
- csharp
- "cpp"
- jscript
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.Diagnostics.Tracing.TraceFunctionEntry
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# TraceFunctionEntry Method (String, String, String, TraceArea)

Records the entry into a function as specified by the parameters.

**Namespace:**  [Microsoft.Web.Media.Diagnostics](microsoft-web-media-diagnostics-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

  Public Shared Sub TraceFunctionEntry ( _
    mediaElementId As String, _
    className As String, _
    methodName As String, _
    traceArea As TraceArea _
)
'Usage

  Dim mediaElementId As String
Dim className As String
Dim methodName As String
Dim traceArea As TraceArea

Tracing.TraceFunctionEntry(mediaElementId, _
    className, methodName, traceArea)
```

```csharp
  public static void TraceFunctionEntry(
    string mediaElementId,
    string className,
    string methodName,
    TraceArea traceArea
)
```

```cpp
  public:
static void TraceFunctionEntry(
    String^ mediaElementId, 
    String^ className, 
    String^ methodName, 
    TraceArea traceArea
)
```

```jscript
  public static function TraceFunctionEntry(
    mediaElementId : String, 
    className : String, 
    methodName : String, 
    traceArea : TraceArea
)
```

### Parameters

  - mediaElementId  
    Type: [System.String](https://msdn.microsoft.com/library/s1wwdcbf)  
    A string value that specifies the ID of the current media element.  

<!-- end list -->

  - className  
    Type: [System.String](https://msdn.microsoft.com/library/s1wwdcbf)  
    A string value that specifies the class name of the calling function.  

<!-- end list -->

  - methodName  
    Type: [System.String](https://msdn.microsoft.com/library/s1wwdcbf)  
    A string value that specifies the name of the calling function.  

<!-- end list -->

  - traceArea  
    Type: [Microsoft.Web.Media.Diagnostics.TraceArea](tracearea-enumeration-microsoft-web-media-diagnostics_1.md)  
    A [TraceArea](tracearea-enumeration-microsoft-web-media-diagnostics_1.md) enumeration object.  

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

[TraceFunctionEntry Overload](tracing-tracefunctionentry-method-microsoft-web-media-diagnostics_1.md)

[Microsoft.Web.Media.Diagnostics Namespace](microsoft-web-media-diagnostics-namespace_1.md)
