---
title: "IAppHostSectionGroup::DeleteSectionGroup Method"
description: "Describes the IAppHostSectionGroup::DeleteSectionGroup Method and details the syntax, parameters, and requirements associated with the method."
ms.date: 10/07/2016
ms.assetid: 39db83f7-5580-2e1f-07dc-cfdaa63241fd
---
# IAppHostSectionGroup::DeleteSectionGroup Method
Removes a configuration section group that is nested under the current configuration section group.  
  
## Syntax  
  
```cpp  
HRESULT DeleteSectionGroup(  
   [in] VARIANT varIndex  
);  
```  
  
### Parameters  
 `varIndex`  
 A `VARIANT` that contains the index of the nested configuration section group to be removed from current configuration section group.  
  
## Return Value  
 An `HRESULT`. Possible values include, but are not limited to, those in the following table.  
  
|Value|Description|  
|-----------|-----------------|  
|S_OK|Indicates that the operation was successful.|  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   IIS 7.0 on [!INCLUDE[winvista](../../wmi-provider/includes/winvista-md.md)]<br />-   IIS 7.5 on Windows 7<br />-   IIS 8.0 on Windows 8<br />-   IIS 10.0 on Windows 10|  
|Server|-   IIS 7.0 on [!INCLUDE[winsrv2008](../../wmi-provider/includes/winsrv2008-md.md)]<br />-   IIS 7.5 on Windows Server 2008 R2<br />-   IIS 8.0 on Windows Server 2012<br />-   IIS 8.5 on Windows Server 2012 R2<br />-   IIS 10.0 on Windows Server 2016|  
|Product|-   IIS 7.0, IIS 7.5, IIS 8.0, IIS 8.5, IIS 10.0<br />-   [!INCLUDE[iisexp75](../../web-development-reference/native-code-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../web-development-reference/native-code-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../web-development-reference/native-code-api-reference/includes/iisexp100-md.md)]|  
|Header|Ahadmin.h|  
  
## See Also  
 [IAppHostSectionGroup Interface](../../web-development-reference/native-code-api-reference/iapphostsectiongroup-interface.md)
