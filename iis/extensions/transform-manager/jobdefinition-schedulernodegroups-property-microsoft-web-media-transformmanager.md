---
title: JobDefinition.SchedulerNodeGroups Property (Microsoft.Web.Media.TransformManager)
TOCTitle: SchedulerNodeGroups Property
description: "The JobDefinition.SchedulerNodeGroups property gets or sets a list of compute nodes. This article describes its syntax and remarks."
ms:assetid: P:Microsoft.Web.Media.TransformManager.JobDefinition.SchedulerNodeGroups
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.transformmanager.jobdefinition.schedulernodegroups(v=VS.90)
ms:contentKeyID: 35520737
ms.date: 06/14/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.TransformManager.JobDefinition.SchedulerNodeGroups
- Microsoft.Web.Media.TransformManager.JobDefinition.get_SchedulerNodeGroups
- Microsoft.Web.Media.TransformManager.JobDefinition.set_SchedulerNodeGroups
dev_langs:
- csharp
- jscript
- vb
- FSharp
- cpp
api_location:
- Microsoft.Web.Media.TransformManager.Common.dll
api_name:
- Microsoft.Web.Media.TransformManager.JobDefinition.get_SchedulerNodeGroups
- Microsoft.Web.Media.TransformManager.JobDefinition.SchedulerNodeGroups
- Microsoft.Web.Media.TransformManager.JobDefinition.set_SchedulerNodeGroups
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# SchedulerNodeGroups Property

Gets or sets a list of compute nodes.

**Namespace:**  [Microsoft.Web.Media.TransformManager](microsoft-web-media-transformmanager-namespace.md)  
**Assembly:**  Microsoft.Web.Media.TransformManager.Common (in Microsoft.Web.Media.TransformManager.Common.dll)

## Syntax

```vb
'Declaration
<DataMemberAttribute> _
Public Property SchedulerNodeGroups As String
    Get
    Set
'Usage

  Dim instance As JobDefinition
Dim value As String

value = instance.SchedulerNodeGroups

instance.SchedulerNodeGroups = value
```

```csharp
[DataMemberAttribute]
public string SchedulerNodeGroups { get; set; }
```

```cpp
[DataMemberAttribute]
public:
property String^ SchedulerNodeGroups {
    String^ get ();
    void set (String^ value);
}
```

``` fsharp
[<DataMemberAttribute>]
member SchedulerNodeGroups : string with get, set
```

```jscript
  function get SchedulerNodeGroups () : String
function set SchedulerNodeGroups (value : String)
```

### Property Value

Type: [System.String](https://msdn.microsoft.com/library/s1wwdcbf)  
The comma-delimited list of compute nodes.  

## Remarks

If the scheduler is an HPC scheduler, the SchedulerNodeGroups property informs the head node to select compute nodes that are in node groups provided by the SchedulerNodeGroups property. The SchedulerNodeGroups property is not validated against the head node.

## See Also

### Reference

[JobDefinition Class](jobdefinition-class-microsoft-web-media-transformmanager.md)

[Microsoft.Web.Media.TransformManager Namespace](microsoft-web-media-transformmanager-namespace.md)
