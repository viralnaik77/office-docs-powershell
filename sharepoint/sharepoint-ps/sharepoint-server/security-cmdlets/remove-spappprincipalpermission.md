---
title: "Remove-SPAppPrincipalPermission"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 866757d6-fcc0-4489-a8d7-a7e0209c293a

description: "Removes the permissions on a specified app principal."
---

# Remove-SPAppPrincipalPermission

Removes the permissions on a specified app principal.
  
```
Remove-SPAppPrincipalPermission -AppPrincipal <SPAppPrincipal> -Scope <Site | SiteCollection | SiteSubscription> -Site <SPWebPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DisableAppOnlyPolicy <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Remove-SPAppPrincipalPermission** cmdlet to remove the permissions on a specified app principal for a given scope (that is, SharePoint Online, site collection, or web). 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppPrincipal** <br/> |Required  <br/> |Microsoft.SharePoint.SPAppPrincipal  <br/> |Specifies the AppPrincipal object to remove.  <br/> |
|**Scope** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPCmdletAppPrincipalPermissionScope  <br/> |Specifies the scope to which to apply the principal permission.  <br/> The value is any of the following scopes:  <br/> --Site  <br/> --Site Collection  <br/> --Site Subscription  <br/> |
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the site (that is, **SPWeb** object) to remove.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DisableAppOnlyPolicy** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies a particular app to disable by turning on a policy.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppPrincipal** <br/> |Required  <br/> |Microsoft.SharePoint.SPAppPrincipal  <br/> ||
|**Scope** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPCmdletAppPrincipalPermissionScope  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DisableAppOnlyPolicy** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------EXAMPLE------------
  
```
$appPrincipal= Get-SPApplicationPrincipal -nameIdentifier $spTrustedIssuer.nameIdentifier -site $site.rootWeb
```

```
Remove-SPAppPrincipalPermission -appPrincipal $appPrincipal -site $site.rootweb -scope "site"
```

This example removes the App Principal permission from the site collection scope.
  
## See also

#### 

[Set-SPAppPrincipalPermission](set-spappprincipalpermission.md)

