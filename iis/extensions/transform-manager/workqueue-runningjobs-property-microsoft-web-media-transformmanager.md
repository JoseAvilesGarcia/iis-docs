---
title: WorkQueue.RunningJobs Property (Microsoft.Web.Media.TransformManager)
description: Describes the RunningJobs property and provides the property's namespace, assembly, syntax, property value, and additional references.
TOCTitle: RunningJobs Property
ms:assetid: P:Microsoft.Web.Media.TransformManager.WorkQueue.RunningJobs
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.transformmanager.workqueue.runningjobs(v=VS.90)
ms:contentKeyID: 35520875
ms.date: 06/14/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.TransformManager.WorkQueue.get_RunningJobs
- Microsoft.Web.Media.TransformManager.WorkQueue.RunningJobs
dev_langs:
- csharp
- jscript
- vb
- FSharp
- cpp
api_location:
- Microsoft.Web.Media.TransformManager.ServiceLibrary.dll
api_name:
- Microsoft.Web.Media.TransformManager.WorkQueue.get_RunningJobs
- Microsoft.Web.Media.TransformManager.WorkQueue.RunningJobs
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# RunningJobs Property

Gets a collection of job details that specify jobs that are running.

**Namespace:**  [Microsoft.Web.Media.TransformManager](microsoft-web-media-transformmanager-namespace.md)  
**Assembly:**  Microsoft.Web.Media.TransformManager.ServiceLibrary (in Microsoft.Web.Media.TransformManager.ServiceLibrary.dll)

## Syntax

```vb
'Declaration

  Public ReadOnly Property RunningJobs As Collection(Of JobDetails)
    Get
'Usage

  Dim instance As WorkQueue
Dim value As Collection(Of JobDetails)

value = instance.RunningJobs
```

```csharp
  public Collection<JobDetails> RunningJobs { get; }
```

```cpp
  public:
property Collection<JobDetails^>^ RunningJobs {
    Collection<JobDetails^>^ get ();
}
```

``` fsharp
  member RunningJobs : Collection<JobDetails>
```

```jscript
  function get RunningJobs () : Collection<JobDetails>
```

### Property Value

Type: [System.Collections.ObjectModel.Collection](https://msdn.microsoft.com/library/ms132397)\< (Of \< ( \<'[JobDetails](jobdetails-class-microsoft-web-media-transformmanager.md)\> ) \> ) \>  
A collection of job details that specify jobs that are running.  

## See Also

### Reference

[WorkQueue Class](workqueue-class-microsoft-web-media-transformmanager.md)

[Microsoft.Web.Media.TransformManager Namespace](microsoft-web-media-transformmanager-namespace.md)
