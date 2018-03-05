---
title: "Add-SPProfileLeader"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 99675c8e-b164-4229-9b8f-eebfda5d5adb

description: "Adds a company leader."
---

# Add-SPProfileLeader

Adds a company leader.
  
```
Add-SPProfileLeader [-ProfileServiceApplicationProxy] <SPServiceApplicationProxyPipeBind> [-Name] <SPProfileLeaderPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-SiteSubscription <SPSiteSubscriptionPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet was introduced in SharePoint Server 2010 with Service Pack 1 (SP1) and SharePoint Foundation 2010 with Service Pack 1 (SP1).
  
Use the **Add-SPProfileLeader** cmdlet to add a user as the company leader. 
  
For additional information about **SPProfileLeader** cmdlets, see [The \*-SPProfileLeader Windows PowerShell cmdlets in SharePoint Server 2010 SP1](https://go.microsoft.com/fwlink/p/?LinkId=226295) (https://go.microsoft.com/fwlink/p/?LinkId=226295). 
  
> [!NOTE]
> After you use the **Add-SPProfileLeader** cmdlet to add a company leader, you have to complete a full crawl of your content sources for the changes to take effect. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ProfileServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the name of the User Profile Service Application Proxy to use.  <br/> |
|**Name** <br/> |Required  <br/> |Microsoft.Office.Server.UserProfiles.PowerShell.SPProfileLeaderPipeBind  <br/> |Specifies the account name to be added as a leader for the new User Profile Service application. For example, Contoso\Joe.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the account under which this service should run. This parameter is mandatory in a hosted-environment and optional in a non-hosted environment.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ProfileServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> ||
|**Name** <br/> |Required  <br/> |Microsoft.Office.Server.UserProfiles.PowerShell.SPProfileLeaderPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------EXAMPLE------------ 
  
```
$upaProxy = Get-SPServiceApplicationProxy 1232b6f7-b9ff-99ad-0cd0-fg1g67h981aq
```

```
Add-SPProfileLeader -ProfileServiceApplicationProxy $upaProxy -Name "contoso\janedow"
```

This example adds a company leader named, Jane Dow.
  
## See also

#### 

[Get-SPProfileLeader](get-spprofileleader.md)
  
[Remove-SPProfileLeader](remove-spprofileleader.md)

