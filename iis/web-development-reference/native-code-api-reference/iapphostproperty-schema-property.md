---
title: "IAppHostProperty::Schema Property"
description: This article contains information about syntax, return value, and requirements for the IAppHostProperty::Schema property. 
ms.date: "10/07/2016"
ms.assetid: 468d6b7a-8fd3-99a4-07a8-3adf433fdfa3
---
# IAppHostProperty::Schema Property
Gets the schema assigned to the current property.  
  
## Syntax  
  
```cpp  
HRESULT get_Schema(  
   [out,  
   retval] IAppHostPropertySchema** ppSchema  
);  
```  
  
### Parameters  
 `ppSchema`  
 A pointer to a pointer for the [IAppHostPropertySchema](../../web-development-reference/native-code-api-reference/iapphostpropertyschema-interface.md) interface that is associated with the current property.  
  
## Return Value  
 An `HRESULT`. Possible values include, but are not limited to, those in the following table.  
  
|Value|Description|  
|-----------|-----------------|  
|S_OK|Indicates that the operation was successful.|  
  
## Remarks  
 This property gets the schema that is used to validate values when the XML configuration is loaded and when the [IAppHostProperty::Value](../../web-development-reference/native-code-api-reference/iapphostproperty-value-property.md) property is set.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   IIS 7.0 on [!INCLUDE[winvista](../../wmi-provider/includes/winvista-md.md)]<br />-   IIS 7.5 on Windows 7<br />-   IIS 8.0 on Windows 8<br />-   IIS 10.0 on Windows 10|  
|Server|-   IIS 7.0 on [!INCLUDE[winsrv2008](../../wmi-provider/includes/winsrv2008-md.md)]<br />-   IIS 7.5 on Windows Server 2008 R2<br />-   IIS 8.0 on Windows Server 2012<br />-   IIS 8.5 on Windows Server 2012 R2<br />-   IIS 10.0 on Windows Server 2016|  
|Product|-   IIS 7.0, IIS 7.5, IIS 8.0, IIS 8.5, IIS 10.0<br />-   [!INCLUDE[iisexp75](../../web-development-reference/native-code-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../web-development-reference/native-code-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../web-development-reference/native-code-api-reference/includes/iisexp100-md.md)]|  
|Header|Ahadmin.h|  
  
## See Also  
 [IAppHostProperty Interface](../../web-development-reference/native-code-api-reference/iapphostproperty-interface.md)
