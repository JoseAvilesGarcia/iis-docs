---
title: "IHttpSite::GetPerfCounterInfo Method"
ms.date: "10/07/2016"
description: The IHttpSite GetPerfCounterInfo Method retrieves an IHttpPerfCounterInfo interface that is used to modify the IIS 7 performance counters at the site level.
ms.assetid: abb697d2-fa6d-8441-ece4-dfb07abd4dee
---
# IHttpSite::GetPerfCounterInfo Method
Retrieves an [IHttpPerfCounterInfo](../../web-development-reference/native-code-api-reference/ihttpperfcounterinfo-interface.md) interface.  
  
## Syntax  
  
```cpp  
virtual IHttpPerfCounterInfo* GetPerfCounterInfo(  
   VOID  
) = 0;  
```  
  
### Parameters  
 This method takes no parameters.  
  
## Return Value  
 A pointer to an `IHttpPerfCounterInfo` interface.  
  
## Remarks  
 The `GetPerfCounterInfo` method retrieves a pointer to an `IHttpPerfCounterInfo` interface that is used to modify the [!INCLUDE[iisver](../../wmi-provider/includes/iisver-md.md)] performance counters at the site level.  
  
> [!IMPORTANT]
>  This method is part of the [!INCLUDE[iisver](../../wmi-provider/includes/iisver-md.md)] infrastructure and is not intended to be used directly from your code.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   IIS 7.0 on [!INCLUDE[winvista](../../wmi-provider/includes/winvista-md.md)]<br />-   IIS 7.5 on Windows 7<br />-   IIS 8.0 on Windows 8<br />-   IIS 10.0 on Windows 10|  
|Server|-   IIS 7.0 on [!INCLUDE[winsrv2008](../../wmi-provider/includes/winsrv2008-md.md)]<br />-   IIS 7.5 on Windows Server 2008 R2<br />-   IIS 8.0 on Windows Server 2012<br />-   IIS 8.5 on Windows Server 2012 R2<br />-   IIS 10.0 on Windows Server 2016|  
|Product|-   IIS 7.0, IIS 7.5, IIS 8.0, IIS 8.5, IIS 10.0<br />-   [!INCLUDE[iisexp75](../../web-development-reference/native-code-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../web-development-reference/native-code-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../web-development-reference/native-code-api-reference/includes/iisexp100-md.md)]|  
|Header|Httpserv.h|  
  
## See Also  
 [IHttpSite Interface](../../web-development-reference/native-code-api-reference/ihttpsite-interface.md)   
 [IHttpPerfCounterInfo Interface](../../web-development-reference/native-code-api-reference/ihttpperfcounterinfo-interface.md)   
 [IHttpServer::GetPerfCounterInfo Method](../../web-development-reference/native-code-api-reference/ihttpserver-getperfcounterinfo-method.md)
