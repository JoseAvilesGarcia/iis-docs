---
title: LocalScheduler.GetRunningJobs Method  (Microsoft.Web.Media.TransformManager)
description: This article contains information on syntax and exceptions for the LocalScheduler.GetRunningJobs method.
TOCTitle: GetRunningJobs Method
ms:assetid: M:Microsoft.Web.Media.TransformManager.LocalScheduler.GetRunningJobs
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.transformmanager.localscheduler.getrunningjobs(v=VS.90)
ms:contentKeyID: 35521130
ms.date: 06/14/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.TransformManager.LocalScheduler.GetRunningJobs
dev_langs:
- csharp
- jscript
- vb
- FSharp
- cpp
api_location:
- Microsoft.Web.Media.TransformManager.Common.dll
api_name:
- Microsoft.Web.Media.TransformManager.LocalScheduler.GetRunningJobs
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# GetRunningJobs Method

Returns a list of job instance IDs based on the currently running jobs.

**Namespace:**  [Microsoft.Web.Media.TransformManager](microsoft-web-media-transformmanager-namespace.md)  
**Assembly:**  Microsoft.Web.Media.TransformManager.Common (in Microsoft.Web.Media.TransformManager.Common.dll)

## Syntax

```vb
'Declaration

  Public Overrides Function GetRunningJobs As ICollection(Of String)
'Usage

  Dim instance As LocalScheduler
Dim returnValue As ICollection(Of String)

returnValue = instance.GetRunningJobs()
```

```csharp
  public override ICollection<string> GetRunningJobs()
```

```cpp
  public:
virtual ICollection<String^>^ GetRunningJobs() override
```

``` fsharp
  abstract GetRunningJobs : unit -> ICollection<string> 
override GetRunningJobs : unit -> ICollection<string> 
```

```jscript
  public override function GetRunningJobs() : ICollection<String>
```

### Return Value

Type: [System.Collections.Generic.ICollection](https://msdn.microsoft.com/library/92t2ye13)\< (Of \< ( \<'[String](https://msdn.microsoft.com/library/s1wwdcbf)\> ) \> ) \>  
A list of job instance IDs.  

## Exceptions

|Exception|Condition|
|--- |--- |
|[COMException](https://msdn.microsoft.com/library/02hkayhc)|The method was unable to complete the transaction that was originated by the task scheduler.|

## See Also

### Reference

[LocalScheduler Class](localscheduler-class-microsoft-web-media-transformmanager.md)

[Microsoft.Web.Media.TransformManager Namespace](microsoft-web-media-transformmanager-namespace.md)
