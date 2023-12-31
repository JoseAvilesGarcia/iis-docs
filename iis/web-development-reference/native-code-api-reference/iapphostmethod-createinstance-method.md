---
title: "IAppHostMethod::CreateInstance Method"
description: Learn how the IAppHostMethod::CreateInstance method provides access to a custom method that is optionally supported on an IAppHostElement Interface object.
ms.date: "10/07/2016"
ms.assetid: 37c391ea-9ce6-48e4-8ecb-cbe7e45b03a0
---
# IAppHostMethod::CreateInstance Method
Provides access to a custom method that is optionally supported on an [IAppHostElement Interface](../../web-development-reference/native-code-api-reference/iapphostelement-interface.md) object.  
  
## Syntax  
  
```cpp  
HRESULT CreateInstance(  
   [out, retval] IAppHostMethodInstance ** ppMethodInstance  
);  
```  
  
### Parameters  
 `ppMethodInstance`  
 Contains the method-created instance.  
  
## Return Value  
 An `HRESULT`. Possible values include, but are not limited to, those in the following table.  
  
|Value|Description|  
|-----------|-----------------|  
|S_OK|Indicates that the operation was successful.|  
  
## Remarks  
 The behavior is analogous to the stack frame of a native method call.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   IIS 7.0 on [!INCLUDE[winvista](../../wmi-provider/includes/winvista-md.md)]<br />-   IIS 7.5 on Windows 7<br />-   IIS 8.0 on Windows 8<br />-   IIS 10.0 on Windows 10|  
|Server|-   IIS 7.0 on [!INCLUDE[winsrv2008](../../wmi-provider/includes/winsrv2008-md.md)]<br />-   IIS 7.5 on Windows Server 2008 R2<br />-   IIS 8.0 on Windows Server 2012<br />-   IIS 8.5 on Windows Server 2012 R2<br />-   IIS 10.0 on Windows Server 2016|  
|Product|-   IIS 7.0, IIS 7.5, IIS 8.0, IIS 8.5, IIS 10.0<br />-   [!INCLUDE[iisexp75](../../web-development-reference/native-code-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../web-development-reference/native-code-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../web-development-reference/native-code-api-reference/includes/iisexp100-md.md)]|  
|Header|Ahadmin.h|  
  
## See Also  
 [IAppHostMethod Interface](../../web-development-reference/native-code-api-reference/iapphostmethod-interface.md)   
 [IAppHostMethodInstance Interface](../../web-development-reference/native-code-api-reference/iapphostmethodinstance-interface.md)
