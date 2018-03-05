---
title: "Set-SPSiteAdministration"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 35f784c0-f74b-49aa-b87d-3b7a3662dd1d

description: "Allows farm administrators to configure any site collection."
---

# Set-SPSiteAdministration

Allows farm administrators to configure any site collection.
  
```
Set-SPSiteAdministration [-Identity] <SPSiteAdministrationPipeBind> [-AdministrationSiteType <None | TenantAdministration>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-LockState <String>] [-MaxSize <Int64>] [-OwnerAlias <SPUserPipeBind>] [-SecondaryOwnerAlias <SPUserPipeBind>] [-Template <SPWebTemplatePipeBind>] [-WarningSize <Int64>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Set-SPSiteAdministration** cmdlet allows a farm administrator to configure particular settings on a site collection even if the farm administrator is not granted explicit permissions. Any parameter that is not provided is not changed. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteAdministrationPipeBind  <br/> |Specifies the URL (full or partial) or GUID of the site collection.  <br/> The type must be a valid URL, in the form http://server_name, or a GUID, in the form 1234-456-987fg.  <br/> |
|**AdministrationSiteType** <br/> |Optional  <br/> |Microsoft.SharePoint.SPAdministrationSiteType  <br/> |Specifies the site type.  <br/> Valid values are **None** or **TentantAdministration**.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Suppresses confirmation messages involved in setting the site subscription. This parameter is used in conjunction with the **SiteSubscription** parameter.  <br/> |
|**LockState** <br/> |Optional  <br/> |System.String  <br/> |Specifies the lock state for the given site collection.  <br/> The type must be any of the following values:  <br/> - **Unlock**: Sets the site collection to unlock.  <br/> - **Content**: No new content can be added. Updates and deletions are allowed.  <br/> - **Readonly**: Sets the site collection to read-only.  <br/> - **Noaccess**: Sets the site collection to unavailable to all users.  <br/> |
|**MaxSize** <br/> |Optional  <br/> |System.Int32  <br/> |Sets the maximum storage size of the site collection.  <br/> The type must be a valid number greater than or equal to 0. .  <br/> Set to 0 for unlimited.  <br/> |
|**OwnerAlias** <br/> |Optional  <br/> |System.String  <br/> |Sets the owner of this site collection.  <br/> The type must be a valid user alias.  <br/> |
|**SecondaryOwnerAlias** <br/> |Optional  <br/> |System.String  <br/> |Sets the secondary owner of this site collection.  <br/> The type must be a valid user alias.  <br/> |
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the Site Group to get site collections.  <br/> |
|**Template** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebTemplatePipeBind  <br/> |Specifies the Web template for the top-level Web site of this site collection. This can only be given if the template has not already been configured.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890abcdef, or an **SPWebTemplate** object.  <br/> |
|**WarningSize** <br/> |Optional  <br/> |System.Int64  <br/> |Specifies the site collection warning size limit.  <br/> The type must be a valid number greater than or equal to 0. Set to 0 for unlimited.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteAdministrationPipeBind  <br/> ||
|**AdministrationSiteType** <br/> |Optional  <br/> |Microsoft.SharePoint.SPAdministrationSiteType  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**LockState** <br/> |Optional  <br/> |System.String  <br/> ||
|**MaxSize** <br/> |Optional  <br/> |System.Int64  <br/> ||
|**OwnerAlias** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUserPipeBind  <br/> ||
|**SecondaryOwnerAlias** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUserPipeBind  <br/> ||
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**Template** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebTemplatePipeBind  <br/> ||
|**WarningSize** <br/> |Optional  <br/> |System.Int64  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
Set-SPSiteAdministration http://sitename -OwnerAlias "DOMAIN\NewOwner"
```

This example allows farm administrators to change the ownership of a site collection to which they do not have access.
  
## See also

#### 

[Get-SPSiteAdministration](get-spsiteadministration.md)
  
[Get-SPSite](get-spsite.md)

