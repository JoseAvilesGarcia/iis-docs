---
title: "IWpfApplicationPreloadUtil::GetApplicationPreloadInfo Method"
description: "Describes the IWpfApplicationPreloadUtil::GetApplicationPreloadInfo method and details its syntax, parameters, return value, and requirements."
ms.date: 10/07/2016
ms.assetid: 7747ae93-976d-4330-8d3a-06bb82180017
---
# IWpfApplicationPreloadUtil::GetApplicationPreloadInfo Method
Returns preload information (such as site ID and virtual path) for an application given the path to its configuration file.  
  
## Syntax  
  
```cpp  
virtual HRESULT GetApplicationPreloadInfo(  
   IN PCWSTR pszConfigPath,  
   OUT BOOL* pfEnabled,  
   OUT BSTR* pbstrType,  
   OUT SAFEARRAY** psaPreloadValues  
) = 0;  
```  
  
### Parameters  
 `pszConfigPath`  
 [IN] Path to the application’s configuration file.  
  
 `pfEnabled`  
 [OUT] Indicates whether preload is enabled for the application.  
  
 `pbstrType`  
 [OUT] Type of the values in the psaPreloadValues array.  
  
 `psaPreloadValues`  
 [OUT] Pointer to an array containing the preload values.  
  
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
|Header|Wpframework.h|  
  
## See Also  
 [IWpfApplicationPreloadUtil Interface](../../web-development-reference/native-code-api-reference/iwpfapplicationpreloadutil-interface.md)
