---
title: "IAppHostConfigLocation::Path Property"
description: Describes the IAppHostConfigLocation::Path property and provides its syntax, parameters, return value, and requirements.
ms.date: "10/07/2016"
ms.assetid: 1abfd93e-a6df-8d5e-565e-ab384be55724
---
# IAppHostConfigLocation::Path Property
Gets the path of the current configuration location.  
  
## Syntax  
  
```cpp  
HRESULT get_Path(  
   [out,  
   string,  
   retval] BSTR* pbstrLocationPath  
);  
```  
  
### Parameters  
 `pbstrLocationPath`  
 A pointer to a `BSTR` that contains the path of the current location.  
  
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
 [IAppHostConfigLocation Interface](../../web-development-reference/native-code-api-reference/iapphostconfiglocation-interface.md)
