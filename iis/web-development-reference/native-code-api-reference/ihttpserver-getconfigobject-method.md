---
title: "IHttpServer::GetConfigObject Method"
description: IHttpServer::GetConfigObject Method retrieves the configuration object for the current context.
ms.date: "10/07/2016"
ms.assetid: 5b9a91b4-edf1-7007-e985-5877c4a89786
---
# IHttpServer::GetConfigObject Method
Retrieves the configuration object for the current context.  
  
## Syntax  
  
```cpp  
virtual INativeConfigurationSystem* GetConfigObject(  
   VOID  
) const = 0;  
```  
  
### Parameters  
 This method takes no parameters.  
  
## Return Value  
 A pointer to an [INativeConfigurationSystem](https://msdn.microsoft.com/ef29f2da-90b4-be7d-e59b-83fa1799f477) interface.  
  
## Remarks  
 The `GetConfigObject` method retrieves a configuration object that you can use to retrieve configuration settings from a configuration file. For example, the [INativeConfigurationSystem::GetConfigSection](https://msdn.microsoft.com/ad4c47fd-a00e-eb0e-f181-0cb41e98c89d) method retrieves a [INativeConfigurationElement](https://msdn.microsoft.com/70c26f09-2188-b797-062a-b2eaca3d9ef7) interface, which is a container object for a section of the configuration settings for the current context. This container object contains several methods that you can use to retrieve or modify the configuration settings.  
  
## Example  
 The following code example demonstrates how to create an HTTP module that uses the [IHttpContext::GetMetadata](../../web-development-reference/native-code-api-reference/ihttpcontext-getmetadata-method.md) method to retrieve a pointer to an [IMetadataInfo](../../web-development-reference/native-code-api-reference/imetadatainfo-interface.md) interface. The module completes the following steps:  
  
1. Uses the [IMetadataInfo::GetMetaPath](../../web-development-reference/native-code-api-reference/imetadatainfo-getmetapath-method.md) method to retrieve the configuration path for the current request.  
  
2. Uses the `GetConfigObject` method to retrieve a pointer to an `INativeConfigurationSystem` interface.  
  
3. Passes the configuration path for the current request to the `INativeConfigurationSystem::GetConfigSection` method.  
  
4. Retrieves an `INativeConfigurationElement` interface for the log settings for IIS.  
  
5. Uses the [INativeConfigurationElement::GetBooleanProperty](https://msdn.microsoft.com/6f2c8f06-b85d-1e93-ab1b-771a6e1e3ca7) method to retrieve a value that indicates whether logging is enabled for the current request context.  
  
6. Returns this information to a Web client and then exits.  
  
 [!code-cpp[IMetadataInfoGetMetaPath#1](../../../samples/snippets/cpp/VS_Snippets_IIS/IIS7/IMetadataInfoGetMetaPath/cpp/IMetadataInfoGetMetaPath.cpp#1)]  
  
 Your module must export the [RegisterModule](../../web-development-reference/native-code-api-reference/pfn-registermodule-function.md) function. You can export this function by creating a module definition (.def) file for your project, or you can compile the module by using the `/EXPORT:RegisterModule` switch. For more information, see [Walkthrough: Creating a Request-Level HTTP Module By Using Native Code](../../web-development-reference/native-code-development-overview/walkthrough-creating-a-request-level-http-module-by-using-native-code.md).  
  
 You can optionally compile the code by using the `__stdcall (/Gz)` calling convention instead of explicitly declaring the calling convention for each function.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   IIS 7.0 on [!INCLUDE[winvista](../../wmi-provider/includes/winvista-md.md)]<br />-   IIS 7.5 on Windows 7<br />-   IIS 8.0 on Windows 8<br />-   IIS 10.0 on Windows 10|  
|Server|-   IIS 7.0 on [!INCLUDE[winsrv2008](../../wmi-provider/includes/winsrv2008-md.md)]<br />-   IIS 7.5 on Windows Server 2008 R2<br />-   IIS 8.0 on Windows Server 2012<br />-   IIS 8.5 on Windows Server 2012 R2<br />-   IIS 10.0 on Windows Server 2016|  
|Product|-   IIS 7.0, IIS 7.5, IIS 8.0, IIS 8.5, IIS 10.0<br />-   [!INCLUDE[iisexp75](../../web-development-reference/native-code-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../web-development-reference/native-code-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../web-development-reference/native-code-api-reference/includes/iisexp100-md.md)]|  
|Header|Httpserv.h|  
  
## See Also  
 [IHttpServer Interface](../../web-development-reference/native-code-api-reference/ihttpserver-interface.md)
