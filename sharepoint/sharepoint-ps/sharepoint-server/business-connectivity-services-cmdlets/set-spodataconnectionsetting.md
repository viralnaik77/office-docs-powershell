---
title: "Set-SPODataConnectionSetting"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 6/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 37d4ceea-fa61-4eb2-9805-2ebc64f4d3eb

description: "Sets or updates global properties for a Microsoft Business Connectivity Services connection."
---

# Set-SPODataConnectionSetting

Sets or updates global properties for a Microsoft Business Connectivity Services connection.
  
```
Set-SPODataConnectionSetting -Name <String> <COMMON PARAMETERS>

```

## Example

-------------EXAMPLE 1----------- 
  
```
Set-SPODataConnectionSetting -Name "ContosoServiceApp" -ServiceContext "http://contoso" -AuthenticationMode "PassThrough" -ExtensionProvider "Contoso.ExtensionProvider.Server, Contoso.ExtensionProvider, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31ba4812ca364d35"
```

This example updates the properties of Business Connectivity Services connection named ContosoServiceApp. 
  
-------------EXAMPLE 2----------- 
  
```
$ConnectionVariable = Get-SPODataConnectionSetting -ServiceContext http://contoso -Name "ContosoServiceApp"
```

```
Set-SPODataConnectionSetting -Identity $ConnectionVariable -AuthenticationMode "PassThrough"
```

This example updates the properties of the Business Connectivity Services service connection named ContosoServiceApp.
  
-------------EXAMPLE 3----------- 
  
```
Set-SPODataConnectionSetting -Name "ContosoServiceApp" -ServiceContext "http://contoso" -AuthenticationMode "PassThrough" -ExtensionProvider ""
```

This example updates the properties of Business Connectivity Services connection named ContosoServiceApp, the authentication mode has been changed, and extension provider value has been cleared.
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
Use the **Set-SPODataConnectionSetting** cmdlet to update the properties of an existing connection for a specific Business Connectivity Services service application. 
  
> [!NOTE]
> This cmdlet applies to an on-premises environment only. You cannot use this command in the SharePoint Online Management Shell. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.SystemSpecific.OData.ODataConnectionSettings  <br/> |Specifies the OData Connection Settings object.  <br/> |
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the existing Business Connectivity Services connection.  <br/> |
| _ServiceContext_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context which is in the form of an instance of an **SPServiceContext** object, an **SPSiteAdministration** object identifier, or a **SPSite** object: An example of a service context value is an identifier from the ID field, a string identifier, a URI, or a string representation of a GUID.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _AuthenticationMode_ <br/> |Optional  <br/> |Microsoft.SharePoint.BusinessData.SystemSpecific.OData.ODataAuthenticationMode  <br/> |Specifies the type of authentication mode that is required for the Business Connectivity Services connection.  <br/> The value for the authentication mode is any one of the following options:  <br/> --PassThrough  <br/> --RevertToSelf  <br/> --Credentials  <br/> --WindowsCredentials  <br/> --DigestCredentials  <br/> --ClientCertificate  <br/> --Anonymous  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _ExtensionProvider_ <br/> |Optional  <br/> |System.String  <br/> |Extends the functionality provided by the OData connector in Business Connectivity Service as well as provides the fully qualified assembly name of an OData extension provider. Fully qualified assembly name should contain following parameters in this order:  <br/> Namespace.Class, Assembly Name, Version, Culture and Public Key. E.g. "Contoso.ExtensionProvider.Server, Contoso.ExtensionPRovider, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31ba4812ca364d35". To clear the value of ExtensionProvider, provide an empty string for example, "".  <br/> |
| _SecureStoreTargetApplicationId_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the Secure Store Target Application ID. Works in conjunction with the **AuthenticationMode** parameter.  <br/> The value for the **SecureStoreTargetApplicationId** parameter is any one of the following options:  <br/> --Credentials  <br/> --WindowsCredentials  <br/> --DigestCredentials  <br/> --ClientCertificate  <br/> |
| _ServiceAddressURL_ <br/> |Optional  <br/> |System.Uri  <br/> |Specifies the URL for the OData service. The URL does not have to be Internet facing. This is the final destination from which data is retrieved.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.SystemSpecific.OData.ODataConnectionSettings  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**AuthenticationMode** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ExtensionProvider** <br/> |Optional  <br/> |System.String  <br/> ||
|**SecureStoreTargetApplicationId** <br/> |Optional  <br/> |System.String  <br/> ||
|**ServiceAddressURL** <br/> |Optional  <br/> |System.Uri  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPODataConnectionSetting](get-spodataconnectionsetting.md)
  
[New-SPODataConnectionSetting](new-spodataconnectionsetting.md)
  
[Remove-SPODataConnectionSetting](remove-spodataconnectionsetting.md)

