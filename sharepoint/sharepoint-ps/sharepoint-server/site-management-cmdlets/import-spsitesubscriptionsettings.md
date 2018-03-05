---
title: "Import-SPSiteSubscriptionSettings"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dd202c04-fa4e-47ff-ad60-59cb5396284d

description: "Restores a backup of subscription site settings to the given subscription identifier."
---

# Import-SPSiteSubscriptionSettings

Restores a backup of subscription site settings to the given subscription identifier.
  
```
Import-SPSiteSubscriptionSettings [-Identity] <SPSiteSubscriptionPipeBind> -Path <String> [-AdminProperties <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Import-SPSiteSubscriptionSettings** cmdlet restores a backup of subscription site settings to the given subscription identifier when the **Identity** parameter is used. To overwrite existing settings, use the **Force** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the ID of the subscription to restore .  <br/> The type must be a valid URL, in the form http://server_name, or a GUID, in the form 1234-4567-985tg.  <br/> |
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies the location of the input file.  <br/> The type must be a valid path, in the form C:\filename.bak.  <br/> |
|**AdminProperties** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that only administrator subscription properties are imported. If this parameter is not set, only non-administrator subscription properties are imported.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |If a setting key already exists, determines whether the value must be overwritten with the value in the backup file.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**AdminProperties** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Get-SPSiteSubscription http://contoso.com | Import-SPSiteSubscriptionSettings -path "c:/backups/contoso_settings_file.bak" -force
```

This example restores the subscription settings store of  `contoso.com`.
  
## See also

#### 

[Export-SPSiteSubscriptionSettings](export-spsitesubscriptionsettings.md)
  
[Remove-SPSiteSubscriptionSettings](remove-spsitesubscriptionsettings.md)

