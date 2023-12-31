---
title: "IHttpConnectionStoredContext::NotifyDisconnect"
ms.date: "10/07/2016"
description: Notify the caller that an established connection was disconnected using required Windows Servers.
ms.assetid: 2b05dd06-6fd9-4754-b5a8-ba63427ff4dc
---
# IHttpConnectionStoredContext::NotifyDisconnect
Notifies the caller that an established connection was disconnected.  
  
## Syntax  
  
```cpp  
virtual VOID NotifyDisconnect(  
   VOID  
) = 0;  
```  
  
### Parameters  
 None  
  
## Return Value  
 `VOID`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   IIS 7.0 on [!INCLUDE[winvista](../../wmi-provider/includes/winvista-md.md)]<br />-   IIS 7.5 on Windows 7<br />-   IIS 8.0 on Windows 8<br />-   IIS 10.0 on Windows 10|  
|Server|-   IIS 7.0 on [!INCLUDE[winsrv2008](../../wmi-provider/includes/winsrv2008-md.md)]<br />-   IIS 7.5 on Windows Server 2008 R2<br />-   IIS 8.0 on Windows Server 2012<br />-   IIS 8.5 on Windows Server 2012 R2<br />-   IIS 10.0 on Windows Server 2016|  
|Product|-   IIS 7.0, IIS 7.5, IIS 8.0, IIS 8.5, IIS 10.0<br />-   [!INCLUDE[iisexp75](../../web-development-reference/native-code-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../web-development-reference/native-code-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../web-development-reference/native-code-api-reference/includes/iisexp100-md.md)]|  
|Header|Httpserv.h|
