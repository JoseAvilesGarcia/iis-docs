---
title: JobScheduler.Save Method  (Microsoft.Web.Media.TransformManager)
description: Describes the Save method and provides the method's namespace, assembly, syntax, parameters, and exceptions.
TOCTitle: Save Method
ms:assetid: M:Microsoft.Web.Media.TransformManager.JobScheduler.Save(System.Boolean)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.transformmanager.jobscheduler.save(v=VS.90)
ms:contentKeyID: 35520667
ms.date: 06/14/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.TransformManager.JobScheduler.Save
dev_langs:
- csharp
- jscript
- vb
- FSharp
- cpp
api_location:
- Microsoft.Web.Media.TransformManager.Common.dll
api_name:
- Microsoft.Web.Media.TransformManager.JobScheduler.Save
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# Save Method

Saves job scheduler details to a file as XML.

**Namespace:**  [Microsoft.Web.Media.TransformManager](microsoft-web-media-transformmanager-namespace.md)  
**Assembly:**  Microsoft.Web.Media.TransformManager.Common (in Microsoft.Web.Media.TransformManager.Common.dll)

## Syntax

```vb
'Declaration

  Public Sub Save ( _
    overwrite As Boolean _
)
'Usage

  Dim instance As JobScheduler
Dim overwrite As Boolean

instance.Save(overwrite)
```

```csharp
  public void Save(
    bool overwrite
)
```

```cpp
  public:
void Save(
    bool overwrite
)
```

``` fsharp
  member Save : 
        overwrite:bool -> unit 
```

```jscript
  public function Save(
    overwrite : boolean
)
```

### Parameters

  - overwrite  
    Type: [System.Boolean](https://msdn.microsoft.com/library/a28wyd50)  
    true to overwrite any existing job template file that has the same name; otherwise, false.  

## Exceptions

|Exception|Condition|
|--- |--- |
|[InvalidOperationException](https://msdn.microsoft.com/library/2asft85a)|The file exists and the overwrite parameter is false.|

## See Also

### Reference

[JobScheduler Class](jobscheduler-class-microsoft-web-media-transformmanager.md)

[Microsoft.Web.Media.TransformManager Namespace](microsoft-web-media-transformmanager-namespace.md)
