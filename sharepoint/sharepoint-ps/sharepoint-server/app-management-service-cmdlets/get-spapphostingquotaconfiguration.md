---
title: "Get-SPAppHostingQuotaConfiguration"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 040c8dd0-56b3-441d-a372-a419d3b810e9

description: "Returns the hosting quotas for an app."
---

# Get-SPAppHostingQuotaConfiguration

Returns the hosting quotas for an app.
  
```
Get-SPAppHostingQuotaConfiguration -Identity <SPSiteSubscriptionPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Get-SPAppHostingQuotaConfiguration** cmdlet to return the hosting quotas for a specified app by using the **Identity** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the site for which to return hosting quotas.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------EXAMPLE 1---------
  
```
Get-SPAppHostingQuotaConfiguration -Identity 586d4a32-98c3-42ce-80be-3c76c10c250c
```

This example returns the hosted app quota associated to SiteSubscriptionID "586d4a32-98c3-42ce-80be-3c76c10c250c".
  
--------------EXAMPLE 2---------
  
```
Get-SPSiteSubscription | Get-SPAppHostingQuotaConfiguration -Identity $_
```

This example returns the hosted app quota associated for all site subscriptions in the farm.
  
## See also

#### 

[Set-SPAppHostingQuotaConfiguration](set-spapphostingquotaconfiguration.md)

