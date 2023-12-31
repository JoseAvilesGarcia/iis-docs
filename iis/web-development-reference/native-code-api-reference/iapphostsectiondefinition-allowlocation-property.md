---
title: IAppHostSectionDefinition::AllowLocation Property
description: Describes the IAppHostSectionDefinition::AllowLocation property and provides the property's syntax, parameters, return value, remarks, and requirements.
ms.date: 10/07/2016
ms.assetid: 8b902a59-f4d5-e223-d8e0-6e5e29f9999d
---
# IAppHostSectionDefinition::AllowLocation Property
Gets or sets a value that indicates whether the configuration section allows the location attribute.  
  
## Syntax  
  
```cpp  
HRESULT get_AllowLocation(  
   [out,  
   retval] BSTR* pbstrAllowLocation  
);  
HRESULT put_AllowLocation(  
   BSTR bstrAllowLocation  
);  
```  
  
### Parameters  
 `pbstrAllowLocation`  
 A pointer to a `BSTR` that indicates whether the configuration section allows the location attribute. Valid values are "true" or "false". The default value is "true".  
  
 `bstrAllowLocation`  
 A `BSTR` that indicates whether the configuration section allows the location attribute. Valid values are "true" or "false".  
  
## Return Value  
 An `HRESULT`. Possible values include, but are not limited to, those in the following table.  
  
|Value|Description|  
|-----------|-----------------|  
|S_OK|Indicates that the operation was successful.|  
  
## Remarks  
  
> [!NOTE]
>  This property uses `BSTR` values of "true" and "false", not `boolean` values of `true` or `false`.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   IIS 7.0 on [!INCLUDE[winvista](../../wmi-provider/includes/winvista-md.md)]<br />-   IIS 7.5 on Windows 7<br />-   IIS 8.0 on Windows 8<br />-   IIS 10.0 on Windows 10|  
|Server|-   IIS 7.0 on [!INCLUDE[winsrv2008](../../wmi-provider/includes/winsrv2008-md.md)]<br />-   IIS 7.5 on Windows Server 2008 R2<br />-   IIS 8.0 on Windows Server 2012<br />-   IIS 8.5 on Windows Server 2012 R2<br />-   IIS 10.0 on Windows Server 2016|  
|Product|-   IIS 7.0, IIS 7.5, IIS 8.0, IIS 8.5, IIS 10.0<br />-   [!INCLUDE[iisexp75](../../web-development-reference/native-code-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../web-development-reference/native-code-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../web-development-reference/native-code-api-reference/includes/iisexp100-md.md)]|  
|Header|Ahadmin.h|  
  
## See Also  
 [IAppHostSectionDefinition Interface](../../web-development-reference/native-code-api-reference/iapphostsectiondefinition-interface.md)
