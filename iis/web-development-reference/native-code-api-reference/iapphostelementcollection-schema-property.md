---
title: IAppHostElementCollection::Schema Property
description: The IAppHostElementCollection::Schema Property returns the schema assigned to the current collection.
ms.date: 10/07/2016
ms.assetid: 31883945-ed20-f557-ea92-e05226340a14
---
# IAppHostElementCollection::Schema Property
Returns the schema assigned to the current collection.  
  
## Syntax  
  
```cpp  
HRESULT get_Schema(  
   [out,  
   retval] IAppHostCollectionSchema** ppSchema  
);  
```  
  
### Parameters  
 `ppSchema`  
 A pointer to a pointer for an [IAppHostCollectionSchema](../../web-development-reference/native-code-api-reference/iapphostcollectionschema-interface.md) interface.  
  
## Return Value  
 An `HRESULT`. Possible values include, but are not limited to, those in the following table.  
  
|Value|Description|  
|-----------|-----------------|  
|S_OK|Indicates that the operation was successful.|  
|E_FAIL|Indicates that the operation was not successful.|  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   IIS 7.0 on [!INCLUDE[winvista](../../wmi-provider/includes/winvista-md.md)]<br />-   IIS 7.5 on Windows 7<br />-   IIS 8.0 on Windows 8<br />-   IIS 10.0 on Windows 10|  
|Server|-   IIS 7.0 on [!INCLUDE[winsrv2008](../../wmi-provider/includes/winsrv2008-md.md)]<br />-   IIS 7.5 on Windows Server 2008 R2<br />-   IIS 8.0 on Windows Server 2012<br />-   IIS 8.5 on Windows Server 2012 R2<br />-   IIS 10.0 on Windows Server 2016|  
|Product|-   IIS 7.0, IIS 7.5, IIS 8.0, IIS 8.5, IIS 10.0<br />-   [!INCLUDE[iisexp75](../../web-development-reference/native-code-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../web-development-reference/native-code-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../web-development-reference/native-code-api-reference/includes/iisexp100-md.md)]|  
|Header|Ahadmin.h|  
  
## See Also  
 [IAppHostElementCollection Interface](../../web-development-reference/native-code-api-reference/iapphostelementcollection-interface.md)
