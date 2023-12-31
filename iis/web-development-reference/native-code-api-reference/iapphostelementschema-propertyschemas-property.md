---
title: "IAppHostElementSchema::PropertySchemas Property"
description: "Describes the IAppHostElementSchema::PropertySchemas property and details its syntax, parameters, return value, and requirements."
ms.date: 10/07/2016
ms.assetid: 93560530-ef5b-4412-aad3-34ea563e7f73
---
# IAppHostElementSchema::PropertySchemas Property
Gets a collection of schemas for the [IAppHostProperty Interface](../../web-development-reference/native-code-api-reference/iapphostproperty-interface.md) objects contained in the corresponding [IAppHostElement Interface](../../web-development-reference/native-code-api-reference/iapphostelement-interface.md) object.  
  
## Syntax  
  
```cpp  
[propget] HRESULT PropertySchemas(  
   [out,  
   retval] IAppHostPropertySchemaCollection * ppPropertySChemas  
);  
```  
  
### Parameters  
 `ppPropertySchemas`  
 Contains the collection of [IAppHostProperty Interface](../../web-development-reference/native-code-api-reference/iapphostproperty-interface.md) schema.  
  
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
|Header|Ahadmin.h|  
  
## See Also  
 [IAppHostElement Interface](../../web-development-reference/native-code-api-reference/iapphostelement-interface.md)   
 [IAppHostElementSchema Interface](../../web-development-reference/native-code-api-reference/iapphostelementschema-interface.md)   
 [IAppHostElementSchemaCollection Interface](../../web-development-reference/native-code-api-reference/iapphostelementschemacollection-interface.md)   
 [IAppHostProperty Interface](../../web-development-reference/native-code-api-reference/iapphostproperty-interface.md)   
 [IAppHostPropertySchema Interface](../../web-development-reference/native-code-api-reference/iapphostpropertyschema-interface.md)   
 [IAppHostPropertySchemaCollection Interface](../../web-development-reference/native-code-api-reference/iapphostpropertyschemacollection-interface.md)
