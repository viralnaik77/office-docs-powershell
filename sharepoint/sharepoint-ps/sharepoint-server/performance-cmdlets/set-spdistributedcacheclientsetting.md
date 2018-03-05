---
title: "Set-SPDistributedCacheClientSetting"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 6/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f503847-e257-49dd-ab4b-f4ea00134753

description: "Sets distributed cache settings."
---

# Set-SPDistributedCacheClientSetting

Sets distributed cache settings.
  
```
Set-SPDistributedCacheClientSetting -ContainerType <DistributedDefaultCache | DistributedAccessCache | DistributedActivityFeedCache | DistributedBouncerCache | DistributedLogonTokenCache | DistributedServerToAppServerAccessTokenCache | DistributedSearchCache | DistributedSecurityTrimmingCache | DistributedActivityFeedLMTCache | DistributedViewStateCache | DistributedSharedWithUserCache | DistributedUnifiedGroupsCache | DistributedFileLockThrottlerCache | DistributedResourceTallyCache | DistributedHealthScoreCache> -DistributedCacheClientSettings <SPDistributedCacheClientSettings> [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

---------EXAMPLE------ 
  
```
$settings = Get-SPDistributedCacheClientSetting -ContainerType DistributedLogonTokenCache
```

```
$settings.MaxConnectionsToServer = 10
```

```
Set-SPDistributedCacheClientSetting -ContainerType DistributedLogonTokenCache -DistributedCacheClientSettings $settings
```

This example updates the MaxConnectionsToServer to 10 for DistributedLogonTokenCache.
  
## Detailed Description

Use the **Set-SPDistributedCacheClientSettings** cmdlet to set the distributed cache service based on usage. Usage can be any type of cache that the **ContainerType** parameter specifies. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ContainerType_ <br/> |Required  <br/> |Microsoft.SharePoint.DistributedCaching.Utilities.SPDistributedCacheContainerType  <br/> | Specifies the container type to clear.  <br/>  The valid values are the following:  <br/>  DistributedDefaultCache  <br/>  DistributedAccessCache  <br/>  DistributedActivityFeedCache  <br/>  DistributedBouncerCache  <br/>  DistributedLogonTokenCache  <br/>  DistributedServerToAppServerAccessTokenCache  <br/>  DistributedSearchCache  <br/>  DistributedSecurityTrimmingCache  <br/>  DistributedActivityFeedLMTCache  <br/>  DistributedViewStateCache  <br/> |
| _DistributedCacheClientSettings_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPDistributedCacheClientSettings  <br/> |Updates the various cache client settings. It is recommended to use the default settings.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ContainerType** <br/> |Required  <br/> |Microsoft.SharePoint.DistributedCaching.Utilities.SPDistributedCacheContainerType  <br/> ||
|**DistributedCacheClientSettings** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPDistributedCacheClientSettings  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[Get-SPDistributedCacheClientSetting](get-spdistributedcacheclientsetting.md)

