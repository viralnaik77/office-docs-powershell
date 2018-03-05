---
title: "Clear-SPDistributedCacheItem"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 6/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae2cbc45-92b2-4704-8531-81c26910ace7

description: "Clears cached items from the distributed cache server."
---

# Clear-SPDistributedCacheItem

Clears cached items from the distributed cache server.
  
```
Clear-SPDistributedCacheItem -ContainerType <DistributedDefaultCache | DistributedAccessCache | DistributedActivityFeedCache | DistributedBouncerCache | DistributedLogonTokenCache | DistributedServerToAppServerAccessTokenCache | DistributedSearchCache | DistributedSecurityTrimmingCache | DistributedActivityFeedLMTCache | DistributedViewStateCache | DistributedSharedWithUserCache | DistributedUnifiedGroupsCache | DistributedFileLockThrottlerCache | DistributedResourceTallyCache | DistributedHealthScoreCache> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------EXAMPLE------
  
```
Clear-SPDistributedCacheItem -ContainerType DistributedLogonTokenCache
```

This example removes all the cache items for distributed token cache.
  
## Detailed Description

Use the **Clear-SPDistributedCacheItems** cmdlet to clear cached items from the distributed cache server. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ContainerType_ <br/> |Required  <br/> |Microsoft.SharePoint.DistributedCaching.Utilities.SPDistributedCacheContainerType  <br/> | Specifies the container type to clear.  <br/>  The valid values are the following:  <br/>  DistributedDefaultCache  <br/>  DistributedAccessCache  <br/>  DistributedActivityFeedCache  <br/>  DistributedBouncerCache  <br/>  DistributedLogonTokenCache  <br/>  DistributedServerToAppServerAccessTokenCache  <br/>  DistributedSearchCache  <br/>  DistributedSecurityTrimmingCache  <br/>  DistributedActivityFeedLMTCache  <br/>  DistributedViewStateCache  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ContainerType** <br/> |Required  <br/> |Microsoft.SharePoint.DistributedCaching.Utilities.SPDistributedCacheContainerType  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   

