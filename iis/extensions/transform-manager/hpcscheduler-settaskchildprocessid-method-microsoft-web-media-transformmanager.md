---
title: HpcScheduler.SetTaskChildProcessId Method  (Microsoft.Web.Media.TransformManager)
description: This article contains information about syntax and parameters for the HpcScheduler.SetTaskChildProcessId method.
TOCTitle: SetTaskChildProcessId Method
ms:assetid: M:Microsoft.Web.Media.TransformManager.HpcScheduler.SetTaskChildProcessId(System.String,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.transformmanager.hpcscheduler.settaskchildprocessid(v=VS.90)
ms:contentKeyID: 35521140
ms.date: 06/14/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.TransformManager.HpcScheduler.SetTaskChildProcessId
dev_langs:
- csharp
- jscript
- vb
- FSharp
- cpp
api_location:
- Microsoft.Web.Media.TransformManager.Common.dll
api_name:
- Microsoft.Web.Media.TransformManager.HpcScheduler.SetTaskChildProcessId
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# SetTaskChildProcessId Method

Sets the child process ID of a child task that is an executable program for the HPC scheduler.

**Namespace:**  [Microsoft.Web.Media.TransformManager](microsoft-web-media-transformmanager-namespace.md)  
**Assembly:**  Microsoft.Web.Media.TransformManager.Common (in Microsoft.Web.Media.TransformManager.Common.dll)

## Syntax

```vb
'Declaration

  Public Overrides Sub SetTaskChildProcessId ( _
    jobInstanceId As String, _
    childProcessId As Integer _
)
'Usage

  Dim instance As HpcScheduler
Dim jobInstanceId As String
Dim childProcessId As Integer

instance.SetTaskChildProcessId(jobInstanceId, _
    childProcessId)
```

```csharp
  public override void SetTaskChildProcessId(
    string jobInstanceId,
    int childProcessId
)
```

```cpp
  public:
virtual void SetTaskChildProcessId(
    String^ jobInstanceId, 
    int childProcessId
) override
```

``` fsharp
  abstract SetTaskChildProcessId : 
        jobInstanceId:string * 
        childProcessId:int -> unit 
override SetTaskChildProcessId : 
        jobInstanceId:string * 
        childProcessId:int -> unit 
```

```jscript
  public override function SetTaskChildProcessId(
    jobInstanceId : String, 
    childProcessId : int
)
```

### Parameters

  - jobInstanceId  
    Type: [System.String](https://msdn.microsoft.com/library/s1wwdcbf)  
    The ID of the job.  

<!-- end list -->

  - childProcessId  
    Type: [System.Int32](https://msdn.microsoft.com/library/td2s409d)  
    The ID of the child process.  

## See Also

### Reference

[HpcScheduler Class](hpcscheduler-class-microsoft-web-media-transformmanager.md)

[Microsoft.Web.Media.TransformManager Namespace](microsoft-web-media-transformmanager-namespace.md)
