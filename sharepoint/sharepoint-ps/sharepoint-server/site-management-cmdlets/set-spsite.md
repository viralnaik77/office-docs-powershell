---
title: "Set-SPSite"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8c7f0ac-52bf-4b79-a356-9d6e485a55aa

description: "Configures the specified sites."
---

# Set-SPSite

Configures the specified sites.
  
```
Set-SPSite [-Identity] <SPSitePipeBind> [-AdministrationSiteType <None | TenantAdministration>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-LockState <String>] [-MaxSize <Int64>] [-OwnerAlias <SPUserPipeBind>] [-QuotaTemplate <SPQuotaTemplatePipeBind>] [-SecondaryOwnerAlias <SPUserPipeBind>] [-SharingType <String>] [-Template <SPWebTemplatePipeBind>] [-Url <String>] [-UserAccountDirectoryPath <String>] [-WarningSize <Int64>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Set-SPSite** cmdlet configures the site collection that is specified by the **Identity** parameter. If a parameter is not used, the value is not changed. 
  
> [!NOTE]
> The **QuotaTemplate** parameter is mutually exclusive to the **MaxSize** parameter and **WarningSize** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the URL or GUID of the site collection to configure, or refers to an **SPSite** object that contains sites to configure.  <br/> The type must be a valid URL, in the form http://server_name; a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an **SPSite** object.  <br/> |
|**AdministrationSiteType** <br/> |Optional  <br/> |Microsoft.SharePoint.SPAdministrationSiteType  <br/> |Specifies the site type.  <br/> Valid values are **None** or **TentantAdministration**.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Suppresses confirmation messages involved in setting the site subscription. This parameter is used in conjunction with the **SiteSubscription** parameter.  <br/> |
|**LockState** <br/> |Optional  <br/> |System.String  <br/> |Sets the lock state of this site collection. The valid lock states are  <br/> **Unlock** Unlocks the site collection and makes it available to users  <br/> **NoAdditions** Prevents users from adding new content to the site collection. Updates and deletions are still allowed  <br/> **ReadOnly** Prevents users from adding, updating, or deleting content.  <br/> **NoAccess** Prevents access to content completely. Users who attempt to access the site receive an access-denied message.  <br/> |
|**MaxSize** <br/> |Optional  <br/> |System.Int32  <br/> |Sets the maximum storage size for the site collection in bytes.  <br/> The integer value must be larger than the **WarningSize** value. You cannot use this parameter if the site collection is using a quota template.  <br/> |
|**OwnerAlias** <br/> |Optional  <br/> |System.String  <br/> |Specifies the alias name of the site collection administrator.  <br/> The type must be a valid e-mail alias, in the form domain\username.  <br/> |
|**QuotaTemplate** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPQuotaTemplatePipeBind  <br/> |Specifies the new quota template for this site collection.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890abcdef or a string  <br/> |
|**SecondaryOwnerAlias** <br/> |Optional  <br/> |System.String  <br/> |Sets the alias of the secondary site collection administrator.  <br/> The type must be a valid e-mail alias, in the form domain\username.  <br/> |
|**SharingType** <br/> |Optional  <br/> |System.String  <br/> |Specifies whether external access a site collection should be disabled, limited to external users only, or enabled for external users and anonymous guests.  <br/> |
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the Site Group to get site collections.  <br/> |
|**Template** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebTemplatePipeBind  <br/> |Specifies the template for this site collection.  <br/>  The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890abcdef.  <br/> |
|**Url** <br/> |Optional  <br/> |System.String  <br/> |Specifies the URL of the new site.  <br/> |
|**UserAccountDirectoryPath** <br/> |Optional  <br/> |String  <br/> |Sets an organization unit to which to scope user accounts.  <br/> |
|**WarningSize** <br/> |Optional  <br/> |System.Int32  <br/> |Sets the storage warning level for the site collection.  <br/> The integer value must be between **0** and the **MaxSize** value. You cannot use this parameter if the site collection is using a quota template.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

------------------EXAMPLE 1---------------------
  
```
Get-SPSite http://sitename/sites/teams/* | Set-SPSite -SecondaryOwnerAlias "DOMAIN\Jdoe"
```

This example sets the secondary owner on a set of site collections to  `DOMAIN\Jdoe`.
  
------------------EXAMPLE 2---------------------
  
```
Set-SPSite -identity "http://sitename" -MaxSize 4000000 -WarningSize 2000000
```

This example configures the Quota settings for the site collection  `http://sitename`.
  
## See also

#### 

[Get-SPSite](get-spsite.md)
  
[New-SPSite](new-spsite.md)
  
[Restore-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/backup-and-recovery-cmdlets/restore-spsite.md)
  
[Remove-SPSite](remove-spsite.md)
  
[Move-SPSite](move-spsite.md)
  
[Restore-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/backup-and-recovery-cmdlets/restore-spsite.md)

