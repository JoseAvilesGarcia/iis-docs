---
title: TransformManagerService.GetJobDefinitions Method  (Microsoft.Web.Media.TransformManager)
description: Describes the GetJobDefinitions method and provides the method's namespace, assembly, syntax, return value, and what the method implements.
TOCTitle: GetJobDefinitions Method
ms:assetid: M:Microsoft.Web.Media.TransformManager.TransformManagerService.GetJobDefinitions
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.transformmanager.transformmanagerservice.getjobdefinitions(v=VS.90)
ms:contentKeyID: 35520887
ms.date: 06/14/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.TransformManager.TransformManagerService.GetJobDefinitions
dev_langs:
- csharp
- jscript
- vb
- FSharp
- cpp
api_location:
- Microsoft.Web.Media.TransformManager.ServiceLibrary.dll
api_name:
- Microsoft.Web.Media.TransformManager.TransformManagerService.GetJobDefinitions
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# GetJobDefinitions Method

Returns all of the [JobDefinition](jobdefinition-class-microsoft-web-media-transformmanager.md) objects from IIS Transform Manager.

**Namespace:**  [Microsoft.Web.Media.TransformManager](microsoft-web-media-transformmanager-namespace.md)  
**Assembly:**  Microsoft.Web.Media.TransformManager.ServiceLibrary (in Microsoft.Web.Media.TransformManager.ServiceLibrary.dll)

## Syntax

```vb
'Declaration
<PrincipalPermissionAttribute(SecurityAction.Demand, Role := "Administrators")> _
Public Function GetJobDefinitions As Collection(Of JobDefinition)
'Usage

  Dim instance As TransformManagerService
Dim returnValue As Collection(Of JobDefinition)

returnValue = instance.GetJobDefinitions()
```

```csharp
[PrincipalPermissionAttribute(SecurityAction.Demand, Role = "Administrators")]
public Collection<JobDefinition> GetJobDefinitions()
```

```cpp
[PrincipalPermissionAttribute(SecurityAction::Demand, Role = L"Administrators")]
public:
virtual Collection<JobDefinition^>^ GetJobDefinitions() sealed
```

``` fsharp
[<PrincipalPermissionAttribute(SecurityAction.Demand, Role = "Administrators")>]
abstract GetJobDefinitions : unit -> Collection<JobDefinition> 
[<PrincipalPermissionAttribute(SecurityAction.Demand, Role = "Administrators")>]
override GetJobDefinitions : unit -> Collection<JobDefinition> 
```

```jscript
  public final function GetJobDefinitions() : Collection<JobDefinition>
```

### Return Value

Type: [System.Collections.ObjectModel.Collection](https://msdn.microsoft.com/library/ms132397)\< (Of \< ( \<'[JobDefinition](jobdefinition-class-microsoft-web-media-transformmanager.md)\> ) \> ) \>  
A collection of [JobDefinition](jobdefinition-class-microsoft-web-media-transformmanager.md) objects.  

### Implements

[IManagementService.GetJobDefinitions() () () ()](imanagementservice-getjobdefinitions-method-microsoft-web-media-transformmanager.md)  

## See Also

### Reference

[TransformManagerService Class](transformmanagerservice-class-microsoft-web-media-transformmanager.md)

[Microsoft.Web.Media.TransformManager Namespace](microsoft-web-media-transformmanager-namespace.md)
