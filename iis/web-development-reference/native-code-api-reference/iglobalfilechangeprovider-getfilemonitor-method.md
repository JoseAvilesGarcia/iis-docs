---
title: "IGlobalFileChangeProvider::GetFileMonitor Method"
description: Learn how the IGlobalFileChangeProvider::GetFileMonitor method returns an IHttpFileMonitor file-change monitor.
ms.date: "10/07/2016"
ms.assetid: 899ac7c8-6596-e1a0-b5b2-4ee7abe6863e
---
# IGlobalFileChangeProvider::GetFileMonitor Method
Returns an [IHttpFileMonitor](../../web-development-reference/native-code-api-reference/ihttpfilemonitor-interface.md) file-change monitor.  
  
## Syntax  
  
```cpp  
virtual IHttpFileMonitor* GetFileMonitor(  
   VOID  
) = 0;  
```  
  
### Parameters  
 This method takes no parameters.  
  
## Return Value  
 A pointer to an `IHttpFileMonitor` interface.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   IIS 7.0 on [!INCLUDE[winvista](../../wmi-provider/includes/winvista-md.md)]<br />-   IIS 7.5 on Windows 7<br />-   IIS 8.0 on Windows 8<br />-   IIS 10.0 on Windows 10|  
|Server|-   IIS 7.0 on [!INCLUDE[winsrv2008](../../wmi-provider/includes/winsrv2008-md.md)]<br />-   IIS 7.5 on Windows Server 2008 R2<br />-   IIS 8.0 on Windows Server 2012<br />-   IIS 8.5 on Windows Server 2012 R2<br />-   IIS 10.0 on Windows Server 2016|  
|Product|-   IIS 7.0, IIS 7.5, IIS 8.0, IIS 8.5, IIS 10.0<br />-   [!INCLUDE[iisexp75](../../web-development-reference/native-code-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../web-development-reference/native-code-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../web-development-reference/native-code-api-reference/includes/iisexp100-md.md)]|  
|Header|Httpserv.h|
