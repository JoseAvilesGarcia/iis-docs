---
title: TraceEntry Constructor  (Microsoft.Web.Media.Diagnostics)
TOCTitle: TraceEntry Constructor
description: Describes the TraceEntry constructor and provides the field's namespace, assembly, syntax, parameters, and version information.
ms:assetid: M:Microsoft.Web.Media.Diagnostics.TraceEntry.#ctor(System.String,System.String,System.String,Microsoft.Web.Media.Diagnostics.TraceArea,Microsoft.Web.Media.Diagnostics.TraceLevel,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.diagnostics.traceentry.traceentry(v=VS.90)
ms:contentKeyID: 23960947
ms.date: 05/02/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.Diagnostics.TraceEntry.#ctor
- Microsoft.Web.Media.Diagnostics.TraceEntry.TraceEntry
dev_langs:
- csharp
- jscript
- vb
- "cpp"
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.Diagnostics.TraceEntry..ctor
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# TraceEntry Constructor

Initializes and new instance of the [TraceEntry](traceentry-class-microsoft-web-media-diagnostics_1.md) class.

**Namespace:**  [Microsoft.Web.Media.Diagnostics](microsoft-web-media-diagnostics-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

  Public Sub New ( _
    mediaElementId As String, _
    className As String, _
    methodName As String, _
    traceArea As TraceArea, _
    traceLevel As TraceLevel, _
    text As String _
)
'Usage

  Dim mediaElementId As String
Dim className As String
Dim methodName As String
Dim traceArea As TraceArea
Dim traceLevel As TraceLevel
Dim text As String

Dim instance As New TraceEntry(mediaElementId, _
    className, methodName, traceArea, _
    traceLevel, text)
```

```csharp
  public TraceEntry(
    string mediaElementId,
    string className,
    string methodName,
    TraceArea traceArea,
    TraceLevel traceLevel,
    string text
)
```

```cpp
  public:
TraceEntry(
    String^ mediaElementId, 
    String^ className, 
    String^ methodName, 
    TraceArea traceArea, 
    TraceLevel traceLevel, 
    String^ text
)
```

```jscript
  public function TraceEntry(
    mediaElementId : String, 
    className : String, 
    methodName : String, 
    traceArea : TraceArea, 
    traceLevel : TraceLevel, 
    text : String
)
```

### Parameters

  - mediaElementId  
    Type: [System.String](https://msdn.microsoft.com/library/s1wwdcbf)  
    String value that specifies the media element ID.  

<!-- end list -->

  - className  
    Type: [System.String](https://msdn.microsoft.com/library/s1wwdcbf)  
    String value that specifies the class name of the method that invoked the trace.  

<!-- end list -->

  - methodName  
    Type: [System.String](https://msdn.microsoft.com/library/s1wwdcbf)  
    String value that specifies the method name of the method that invoked the trace.  

<!-- end list -->

  - traceArea  
    Type: [Microsoft.Web.Media.Diagnostics.TraceArea](tracearea-enumeration-microsoft-web-media-diagnostics_1.md)  
    A [TraceArea](tracearea-enumeration-microsoft-web-media-diagnostics_1.md) enumeration object.  

<!-- end list -->

  - traceLevel  
    Type: [Microsoft.Web.Media.Diagnostics.TraceLevel](tracelevel-enumeration-microsoft-web-media-diagnostics_1.md)  
    A [TraceLevel](tracelevel-enumeration-microsoft-web-media-diagnostics_1.md) enumeration object.  

<!-- end list -->

  - text  
    Type: [System.String](https://msdn.microsoft.com/library/s1wwdcbf)  
    String value that specifies the text description of the trace.  

## Version Information

### Silverlight

Supported in: 4  

### Silverlight for Windows Phone

Supported in: Windows Phone OS 7.0  

## Permissions

  - Full trust for the immediate caller. This member cannot be used by partially trusted code. For more information, see [Using Libraries from Partially Trusted Code](https://msdn.microsoft.com/library/8skskf63).

## See Also

### Reference

[TraceEntry Class](traceentry-class-microsoft-web-media-diagnostics_1.md)

[Microsoft.Web.Media.Diagnostics Namespace](microsoft-web-media-diagnostics-namespace_1.md)
