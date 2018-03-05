---
title: "Remove-SPODataConnectionSetting"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ef3e600-4590-4ae7-a622-e2ee046f3d48

description: "Removes a Business Connectivity Services connection."
---

# Remove-SPODataConnectionSetting

Removes a Business Connectivity Services connection.
  
```
Remove-SPODataConnectionSetting -Name <String> -ServiceContext <SPServiceContextPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **Remove-SPODataConnectionSetting** cmdlet to remove a Business Connectivity Services connection for a particular Business Connectivity Services service application in the farm. 
  
The metadata object associated with the Business Connectivity Services connection is also deleted.
  
> [!NOTE]
> This cmdlet applies to an on-premises environment only. You cannot use this command in the SharePoint Online Management Shell. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.SystemSpecific.OData.ODataConnectionSettings  <br/> |Specifies the OData Connection Settings object.  <br/> |
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context which is in the form of an instance of an **SPServiceContext** object, an **SPSiteAdministration** object identifier, or a **SPSite** object. An example of a service context value is an identifier from the ID field, a string identifier, a URI, or a string representation of a GUID.  <br/> |
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the existing Business Connectivity Services connection.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.SystemSpecific.OData.ODataConnectionSettings  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.SystemSpecific.OData.ODataConnectionSettings  <br/> ||
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**Title** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

----------------EXAMPLE 1------------
  
```
Remove-SPODataConnectionSetting -ServiceContext "http://contoso" -Name "ContosoServiceApp"
```

This example removes the Business Connectivity Services connection named **ContosoServiceApp**. Metadata properties are also removed.
  
----------------EXAMPLE 2------------
  
```
Remove-SPODataConnectionSetting -ServiceContext "http://contoso" -Name "ContosoServiceApp-metadata"
```

This example removes the Business Connectivity Services connection metadata named **ContosoServiceApp**.
  
The associated Business Connectivity Services connection object is also removed.
  
----------------EXAMPLE 3------------
  
```
$ConnectionVariable = Get-SPODataConnectionSettingMetadata -ServiceContext http://contoso -Name "ContosoServiceApp"
```

```
Remove-SPODataConnectionSetting -Identity $ConnectionVariable -ServiceContext "http://contoso"
```

This example removes the Business Connectivity Services and its associated metadata connection named **ContosoServiceApp**.
  
## See also

#### 

[Get-SPODataConnectionSetting](get-spodataconnectionsetting.md)
  
[New-SPODataConnectionSetting](new-spodataconnectionsetting.md)
  
[Set-SPODataConnectionSetting](set-spodataconnectionsetting.md)

