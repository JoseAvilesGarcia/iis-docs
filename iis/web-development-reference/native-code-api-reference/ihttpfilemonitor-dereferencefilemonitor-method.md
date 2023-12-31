---
title: IHttpFileMonitor::DereferenceFileMonitor Method
description: The IHttpFileMonitor::DereferenceFileMonitor Method releases a file monitor interface. 
ms.date: 10/07/2016
ms.assetid: 13610ef2-eadf-2dfe-cb84-aad275c0e8bb
---
# IHttpFileMonitor::DereferenceFileMonitor Method
Releases a file monitor interface.  
  
## Syntax  
  
```cpp  
virtual VOID DereferenceFileMonitor(  
   VOID  
) = 0;  
```  
  
### Parameters  
 This method takes no parameters.  
  
## Return Value  
 VOID.  
  
## Remarks  
 [IHttpFileMonitor](../../web-development-reference/native-code-api-reference/ihttpfilemonitor-interface.md)  
  
## Example  
  
```  
N/A  
```  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   IIS 7.0 on [!INCLUDE[winvista](../../wmi-provider/includes/winvista-md.md)]<br />-   IIS 7.5 on Windows 7<br />-   IIS 8.0 on Windows 8<br />-   IIS 10.0 on Windows 10|  
|Server|-   IIS 7.0 on [!INCLUDE[winsrv2008](../../wmi-provider/includes/winsrv2008-md.md)]<br />-   IIS 7.5 on Windows Server 2008 R2<br />-   IIS 8.0 on Windows Server 2012<br />-   IIS 8.5 on Windows Server 2012 R2<br />-   IIS 10.0 on Windows Server 2016|  
|Product|-   IIS 7.0, IIS 7.5, IIS 8.0, IIS 8.5, IIS 10.0<br />-   [!INCLUDE[iisexp75](../../web-development-reference/native-code-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../web-development-reference/native-code-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../web-development-reference/native-code-api-reference/includes/iisexp100-md.md)]|  
|Header|Httpserv.h|  
  
## See Also  
 [IHttpFileMonitor Interface](../../web-development-reference/native-code-api-reference/ihttpfilemonitor-interface.md)
