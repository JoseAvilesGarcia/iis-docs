---
title: "IHttpCacheKey::Enum Method"
description: "Describes the IHttpCacheKey::Enum method and details its syntax, parameters, remarks, and requirements." 
ms.date: 10/07/2016
ms.assetid: 979f5cae-7487-de8b-2d93-7aab5b396862
---
# IHttpCacheKey::Enum Method
Enumerates an [IHttpCacheSpecificData](../../web-development-reference/native-code-api-reference/ihttpcachespecificdata-interface.md) pointer.  
  
## Syntax  
  
```cpp  
virtual VOID Enum(  
   IHttpCacheSpecificData* cacheData  
) = 0;  
```  
  
### Parameters  
 `cacheData`  
 A pointer to an `IHttpCacheSpecificData` value.  
  
## Remarks  
 The `Enum` method behavior depends on both interface and implementation. You should use the following information as a guideline, but it may not be correct in all scenarios:  
  
 All current `IHttpCacheSpecificData`, [IFileKey](../../web-development-reference/native-code-api-reference/ifilekey-interface.md), [IHttpTokenKey](../../web-development-reference/native-code-api-reference/ihttptokenkey-interface.md), and [IUriKey](../../web-development-reference/native-code-api-reference/iurikey-interface.md) implementers perform empty operations on the `Enum` method.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   IIS 7.0 on [!INCLUDE[winvista](../../wmi-provider/includes/winvista-md.md)]<br />-   IIS 7.5 on Windows 7<br />-   IIS 8.0 on Windows 8<br />-   IIS 10.0 on Windows 10|  
|Server|-   IIS 7.0 on [!INCLUDE[winsrv2008](../../wmi-provider/includes/winsrv2008-md.md)]<br />-   IIS 7.5 on Windows Server 2008 R2<br />-   IIS 8.0 on Windows Server 2012<br />-   IIS 8.5 on Windows Server 2012 R2<br />-   IIS 10.0 on Windows Server 2016|  
|Product|-   IIS 7.0, IIS 7.5, IIS 8.0, IIS 8.5, IIS 10.0<br />-   [!INCLUDE[iisexp75](../../web-development-reference/native-code-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../web-development-reference/native-code-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../web-development-reference/native-code-api-reference/includes/iisexp100-md.md)]|  
|Header|Httpserv.h|  
  
## See Also  
 [IHttpCacheKey Interface](../../web-development-reference/native-code-api-reference/ihttpcachekey-interface.md)
