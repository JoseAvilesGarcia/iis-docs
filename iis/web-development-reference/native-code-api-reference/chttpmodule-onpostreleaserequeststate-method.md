---
title: CHttpModule::OnPostReleaseRequestState Method
description: Describes the CHttpModule::OnPostReleaseRequestState method and provides the method's syntax, return value, remarks, an example, and requirements.
ms.date: 10/07/2016
ms.assetid: 0996da55-cb9b-03aa-84e0-a3ac12360ee7
---
# CHttpModule::OnPostReleaseRequestState Method
Represents the method that will handle a `ReleaseRequestState` post-event, which occurs after the current state has been released.  
  
## Syntax  
  
```cpp  
virtual REQUEST_NOTIFICATION_STATUS OnPostReleaseRequestState(  
   IN IHttpContext* pHttpContext,  
   IN IHttpEventProvider* pProvider  
);  
```  
  
### Parameters  
 `pHttpContext`  
 [IN] A pointer to an [IHttpContext](../../web-development-reference/native-code-api-reference/ihttpcontext-interface.md) interface.  
  
 `pProvider`  
 [IN] A pointer to an [IHttpEventProvider](../../web-development-reference/native-code-api-reference/ihttpeventprovider-interface.md) interface.  
  
## Return Value  
 A [REQUEST_NOTIFICATION_STATUS](../../web-development-reference/native-code-api-reference/request-notification-status-enumeration.md) value.  
  
## Remarks  
 When a request-level module is registered for the [RQ_RELEASE_REQUEST_STATE](../../web-development-reference/native-code-api-reference/request-processing-constants.md) post-event notification, IIS will call the module's `OnReleaseRequestState` method after it has released the state for current request.  
  
> [!NOTE]
>  Request-level modules can register for the `ReleaseRequestState` post-event notification by registering for `RQ_RELEASE_REQUEST_STATE` in the module's [RegisterModule](../../web-development-reference/native-code-api-reference/pfn-registermodule-function.md) function.  
  
## Example  
 The following code example demonstrates how to create a request-level HTTP module that registers for the `RQ_RELEASE_REQUEST_STATE` event and post-event notifications. When IIS releases the state for current request, it will call the example module's [OnReleaseRequestState](../../web-development-reference/native-code-api-reference/chttpmodule-onreleaserequeststate-method.md) and `OnPostReleaseRequestState` methods. Each method will write an entry in the application log of the Windows Event Viewer. When processing is complete, the module will exit.  
  
 [!code-cpp[CHttpModuleReleaseRequestState#1](../../../samples/snippets/cpp/VS_Snippets_IIS/IIS7/CHttpModuleReleaseRequestState/cpp/CHttpModuleReleaseRequestState.cpp#1)]  
  
 Your module must export the `RegisterModule` function. You can export this function by creating a module definition (.def) file for your project, or you can compile the module by using the `/EXPORT:RegisterModule` switch. For more information, see [Walkthrough: Creating a Request-Level HTTP Module By Using Native Code](../../web-development-reference/native-code-development-overview/walkthrough-creating-a-request-level-http-module-by-using-native-code.md).  
  
 You can optionally compile the code by using the `__stdcall (/Gz)` calling convention instead of explicitly declaring the calling convention for each function.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   IIS 7.0 on [!INCLUDE[winvista](../../wmi-provider/includes/winvista-md.md)]<br />-   IIS 7.5 on Windows 7<br />-   IIS 8.0 on Windows 8<br />-   IIS 10.0 on Windows 10|  
|Server|-   IIS 7.0 on [!INCLUDE[winsrv2008](../../wmi-provider/includes/winsrv2008-md.md)]<br />-   IIS 7.5 on Windows Server 2008 R2<br />-   IIS 8.0 on Windows Server 2012<br />-   IIS 8.5 on Windows Server 2012 R2<br />-   IIS 10.0 on Windows Server 2016|  
|Product|-   IIS 7.0, IIS 7.5, IIS 8.0, IIS 8.5, IIS 10.0<br />-   [!INCLUDE[iisexp75](../../web-development-reference/native-code-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../web-development-reference/native-code-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../web-development-reference/native-code-api-reference/includes/iisexp100-md.md)]|  
|Header|Httpserv.h|  
  
## See Also  
 [CHttpModule Class](../../web-development-reference/native-code-api-reference/chttpmodule-class.md)   
 [CHttpModule::OnReleaseRequestState Method](../../web-development-reference/native-code-api-reference/chttpmodule-onreleaserequeststate-method.md)
