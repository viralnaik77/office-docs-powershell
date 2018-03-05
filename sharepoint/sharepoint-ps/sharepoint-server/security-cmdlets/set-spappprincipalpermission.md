---
title: "Set-SPAppPrincipalPermission"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ada83c3d-dc0f-4b55-addf-8fde2c1e8457

description: "Sets the permissions on a given app principal."
---

# Set-SPAppPrincipalPermission

Sets the permissions on a given app principal.
  
```
Set-SPAppPrincipalPermission -AppPrincipal <SPAppPrincipal> -Right <Read | Write | Manage | FullControl> -Scope <Site | SiteCollection | SiteSubscription> -Site <SPWebPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-EnableAppOnlyPolicy <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Set-SPAppPrincipalPermission** cmdlet to set the permissions on a given app principal for a given scope (Site, site collection, or Site Subscription) and given levels (Read, Write, Manage, Full Control). 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppPrincipal** <br/> |Required  <br/> |Microsoft.SharePoint.SPAppPrincipal  <br/> |Specifies the AppPrincipal object.  <br/> |
|**Right** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPCmdletAppPrincipalPermissionKind  <br/> |Specifies the permission level for the principal object.  <br/> The value is any of the following levels:  <br/> -- **Read** <br/> -- **Write** <br/> -- **Manage** <br/> -- **Full Control** <br/> |
|**Scope** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPCmdletAppPrincipalPermissionScope  <br/> |Specifies the scope to which to apply the principal permission.  <br/> The value is any of the following scopes:  <br/> Site  <br/> Site collection  <br/> SiteSubscription  <br/> |
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the site (that is, SPWeb object) that the AppPrincipalPermission is being set.  <br/> |
|**EnableAppOnlyPolicy** <br/> ||System.Management.Automation.SwitchParameter  <br/> |Specifies if the app only policy is turned on for the app principal.  <br/> The valid values are **True** and **False**. The default value is **False**.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppPrincipal** <br/> |Required  <br/> |Microsoft.SharePoint.SPAppPrincipal  <br/> ||
|**Right** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPCmdletAppPrincipalPermissionKind  <br/> ||
|**Scope** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPCmdletAppPrincipalPermissionScope  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**EnableAppOnlyPolicy** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------EXAMPLE-------------
  
```
$appPrincipal= Get-SPApplicationPrincipal -nameIdentifier $spTrustedIssuer.nameIdentifier -web $site.rootWeb
```

```
Set-AppPrincipalPermission -appPrincipal $appPrincipal -site $site.rootweb -scope "spweb" -level "WRITE"
```

This example sets the **Write** permission level of to the **SPWeb** scope. 
  
## See also

#### 

[Remove-SPAppPrincipalPermission](remove-spappprincipalpermission.md)

