---
title: "IProcessHost::Shutdown Method"
description: Learn how the IProcessHost::Shutdown method sends a request to terminate all applications in an application domain.
ms.date: "10/07/2016"
ms.assetid: ed5720ca-5927-4117-c287-ba5cdac43340
---
# IProcessHost::Shutdown Method
Sends a request to terminate all applications in an application domain.  
  
## Syntax  
  
```cpp  
virtual HRESULT __stdcall Shutdown(  
) = 0;  
```  
  
### Parameters  
 This method takes no parameters.  
  
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
 [IProcessHost Interface](../../web-development-reference/native-code-api-reference/iprocesshost-interface.md)   
 [IIS 7.0 Beta: IProcessHost::Shutdown Method](../../web-development-reference/native-code-api-reference/iprocesshost-shutdown-method.md)   
 [IProcessHost::StartApplication Method](../../web-development-reference/native-code-api-reference/iprocesshost-startapplication-method.md)
