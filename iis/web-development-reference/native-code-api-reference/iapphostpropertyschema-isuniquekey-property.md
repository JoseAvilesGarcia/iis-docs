---
title: "IAppHostPropertySchema::IsUniqueKey Property"
description: Learn how the IsUniqueKey property determines whether a property value is a unique key for a collection.
ms.date: "10/07/2016"
ms.assetid: 8ab3c522-03ae-4d2f-daf4-e82086b6c1a2
---
# IAppHostPropertySchema::IsUniqueKey Property
Determines whether a property value is a unique key for a collection.  
  
## Syntax  
  
```cpp  
HRESULT get_IsUniqueKey(  
   [out,  
   retval] VARIANT_BOOL* pfIsUniqueKey  
);  
```  
  
### Parameters  
 `pfIsUniqueKey`  
 A pointer to a `VARIANT_BOOL`. `VARIANT_TRUE` if a property value is a unique key for a collection; otherwise, `VARIANT_FALSE`. The default is `VARIANT_FALSE`.  
  
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
 [IAppHostPropertySchema Interface](../../web-development-reference/native-code-api-reference/iapphostpropertyschema-interface.md)   
 [IAppHostPropertySchema::IsCombinedKey Property](../../web-development-reference/native-code-api-reference/iapphostpropertyschema-iscombinedkey-property.md)
