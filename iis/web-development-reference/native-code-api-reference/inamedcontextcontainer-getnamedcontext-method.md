---
title: "INamedContextContainer::GetNamedContext Method"
description: Learn how the GetNamedContext method retrieves a stored context given its name.
ms.date: "10/07/2016"
ms.assetid: 639f9b9d-8141-41ce-97cd-4e623090a602
---
# INamedContextContainer::GetNamedContext Method
Retrieves a stored context given its name.  
  
## Syntax  
  
```cpp  
Virtual IHttpStoredContext * GetNamedContext(  
   _In_ LPCWSTR szName  
) = 0;  
```  
  
### Parameters  
 `szName`  
 [IN] The name of the context.  
  
## Return Value  
 A pointer to a [IHttpStoredContext](../../web-development-reference/native-code-api-reference/ihttpstoredcontext-interface.md) object.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   IIS 7.0 on [!INCLUDE[winvista](../../wmi-provider/includes/winvista-md.md)]<br />-   IIS 7.5 on Windows 7<br />-   IIS 8.0 on Windows 8<br />-   IIS 10.0 on Windows 10|  
|Server|-   IIS 7.0 on [!INCLUDE[winsrv2008](../../wmi-provider/includes/winsrv2008-md.md)]<br />-   IIS 7.5 on Windows Server 2008 R2<br />-   IIS 8.0 on Windows Server 2012<br />-   IIS 8.5 on Windows Server 2012 R2<br />-   IIS 10.0 on Windows Server 2016|  
|Product|-   IIS 7.0, IIS 7.5, IIS 8.0, IIS 8.5, IIS 10.0<br />-   [!INCLUDE[iisexp75](../../web-development-reference/native-code-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../web-development-reference/native-code-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../web-development-reference/native-code-api-reference/includes/iisexp100-md.md)]|  
|Header|Httpserv.h|  
  
## See Also  
 [INamedContextContainer Interface](../../web-development-reference/native-code-api-reference/inamedcontextcontainer-interface.md)
