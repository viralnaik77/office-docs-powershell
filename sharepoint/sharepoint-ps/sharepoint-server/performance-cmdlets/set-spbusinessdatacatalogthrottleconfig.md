---
title: "Set-SPBusinessDataCatalogThrottleConfig"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4462b0a3-f163-46b6-b78e-da10418dd202

description: "Sets the throttling configuration for a Business Data Connectivity Service application."
---

# Set-SPBusinessDataCatalogThrottleConfig

Sets the throttling configuration for a Business Data Connectivity Service application.
  
```
Set-SPBusinessDataCatalogThrottleConfig -Default <Int32> -Identity <ThrottleConfig> -Maximum <Int32> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Set-SPBusinessDataCatalogThrottleConfig** cmdlet sets the throttling configuration for a Business Data Connectivity Service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Default** <br/> |Required  <br/> |System.Int32  <br/> |Specifies the default setting of the throttle configuration.  <br/> |
|**Enforced** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the throttle configuration setting cannot be overridden.  <br/> |
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.SharedService.ThrottleConfig  <br/> |Specifies the throttle configuration to update.  <br/> |
|**Maximum** <br/> |Required  <br/> |System.Int32  <br/> |Specifies the maximum value of the throttling configuration setting.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Default** <br/> |Required  <br/> |System.Int32  <br/> ||
|**Enforced** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.SharedService.ThrottleConfig  <br/> ||
|**Maximum** <br/> |Required  <br/> |System.Int32  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Get-SPBusinessDataCatalogThrottleConfig -Scope Database -ThrottleType Items -ServiceApplicationProxy $contosoServAppProxy | Set-SPBusinessDataCatalogThrottleConfig -Maximum 1000000000 -Default 500000
```

This example sets the database item throttling to values of  `1000000000` maximum and  `500000` default for the given service application. 
  
## See also

#### 

[Get-SPBusinessDataCatalogThrottleConfig](get-spbusinessdatacatalogthrottleconfig.md)

