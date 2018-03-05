---
title: "Remove-SPProfileLeader"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/8/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98917425-b3df-4191-b2f4-81a336cd8f38

description: "Remove a company leader."
---

# Remove-SPProfileLeader

Remove a company leader.
  
```
Remove-SPProfileLeader [-ProfileServiceApplicationProxy] <SPServiceApplicationProxyPipeBind> [-Name] <SPProfileLeaderPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-SiteSubscription <SPSiteSubscriptionPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet was introduced in SharePoint Server 2010 with Service Pack 1 (SP1) and SharePoint Foundation 2010 with Service Pack 1 (SP1).
  
Use the **Remove-SPProfileLeader** cmdlet to remove a user as the company leader. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ProfileServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the name of the User Profile Service Application Proxy to use.  <br/> |
|**Name** <br/> |Required  <br/> |Microsoft.Office.Server.UserProfiles.PowerShell.SPProfileLeaderPipeBind  <br/> |Specifies the account name to be removed as a leader for the new User Profile Service application. For example, Contoso\Joe.  <br/> |
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

---------------EXAMPLE------------ 
  
```
$upaProxy = Get-SPServiceApplicationProxy 1232b6f7-b9ff-99ad-0cd0-fg1g67h981aq
```

```
Remove-SPProfileLeader -ProfileServiceApplicationProxy $upaProxy -Name "contoso\janedow"
```

This example removes the user "Jane Dow" from the leaders list for a specific user profile service application.
  
## See also

#### 

[Add-SPProfileLeader](add-spprofileleader.md)
  
[Get-SPProfileLeader](get-spprofileleader.md)

