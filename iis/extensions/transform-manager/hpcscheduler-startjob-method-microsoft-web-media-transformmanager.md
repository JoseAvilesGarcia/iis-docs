---
title: HpcScheduler.StartJob Method  (Microsoft.Web.Media.TransformManager)
description: Details the syntax for using the StartJob method which starts the specified job using the HPC scheduler.
TOCTitle: StartJob Method
ms:assetid: M:Microsoft.Web.Media.TransformManager.HpcScheduler.StartJob(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.transformmanager.hpcscheduler.startjob(v=VS.90)
ms:contentKeyID: 35520573
ms.date: 06/14/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.TransformManager.HpcScheduler.StartJob
dev_langs:
- csharp
- jscript
- vb
- FSharp
- cpp
api_location:
- Microsoft.Web.Media.TransformManager.Common.dll
api_name:
- Microsoft.Web.Media.TransformManager.HpcScheduler.StartJob
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# StartJob Method

Starts the specified job using the HPC scheduler.

**Namespace:**  [Microsoft.Web.Media.TransformManager](microsoft-web-media-transformmanager-namespace.md)  
**Assembly:**  Microsoft.Web.Media.TransformManager.Common (in Microsoft.Web.Media.TransformManager.Common.dll)

## Syntax

```vb
'Declaration

  Public Overrides Function StartJob ( _
    jobInstanceId As String _
) As JobStatus
'Usage

  Dim instance As HpcScheduler
Dim jobInstanceId As String
Dim returnValue As JobStatus

returnValue = instance.StartJob(jobInstanceId)
```

```csharp
  public override JobStatus StartJob(
    string jobInstanceId
)
```

```cpp
  public:
virtual JobStatus StartJob(
    String^ jobInstanceId
) override
```

``` fsharp
  abstract StartJob : 
        jobInstanceId:string -> JobStatus 
override StartJob : 
        jobInstanceId:string -> JobStatus 
```

```jscript
  public override function StartJob(
    jobInstanceId : String
) : JobStatus
```

### Parameters

  - jobInstanceId  
    Type: [System.String](https://msdn.microsoft.com/library/s1wwdcbf)  
    The ID of the job.  

### Return Value

Type: [Microsoft.Web.Media.TransformManager.JobStatus](jobstatus-enumeration-microsoft-web-media-transformmanager.md)  
The status information about the job.  

## See Also

### Reference

[HpcScheduler Class](hpcscheduler-class-microsoft-web-media-transformmanager.md)

[Microsoft.Web.Media.TransformManager Namespace](microsoft-web-media-transformmanager-namespace.md)
