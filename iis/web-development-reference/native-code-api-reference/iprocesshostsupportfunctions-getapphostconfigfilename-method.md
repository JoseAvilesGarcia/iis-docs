---
title: "IProcessHostSupportFunctions::GetAppHostConfigFilename Method"
ms.date: "10/07/2016"
description: IProcessHostSupportFunctions GetAppHostConfigFilename Method retrieves the application host configuration (.config) file path.
ms.assetid: 781a6b10-ce53-5a78-8d63-7be92a3ba4a1
---
# IProcessHostSupportFunctions::GetAppHostConfigFilename Method
Retrieves the application host configuration (.config) file path.  
  
## Syntax  
  
```cpp  
virtual HRESULT __stdcall GetAppHostConfigFilename(  
   BSTR* pbstrPhysicalPath  
) = 0;  
```  
  
### Parameters  
 `pbstrPhysicalPath`  
 A pointer to a `BSTR` that contains the physical path (including the file name) to the application host configuration file.  
  
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
|Header|Webhost.h|  
  
## See Also  
 [IProcessHostSupportFunctions Interface](../../web-development-reference/native-code-api-reference/iprocesshostsupportfunctions-interface.md)
