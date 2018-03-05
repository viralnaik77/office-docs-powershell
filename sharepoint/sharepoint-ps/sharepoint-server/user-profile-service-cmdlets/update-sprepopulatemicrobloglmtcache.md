---
title: "Update-SPRepopulateMicroblogLMTCache"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d1557d81-7bac-47ca-84bc-27d891e160eb

description: "Refreshes the cache."
---

# Update-SPRepopulateMicroblogLMTCache

Refreshes the cache.
  
```
Update-SPRepopulateMicroblogLMTCache -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

------------EXAMPLE-----------
  
```
Update-SPRepopulateMicroblogLMTCache -ProfileServiceApplicationProxy a4f93369-0795-4aee-8a21-46f5ade29606
```

This example refreshes the cache for the specified proxy.
  
## Detailed Description

Use the **Update-SPRepopulateMicroblogLMTCache** cmdlet to refresh when the **Feed Cache Repopulation Job** timer job fails to work. The **Update-SPRepopulateMicroblogLMTCache** cmdlet forcefully refreshes the last modified times of all the known persisted entities to FeedCache. 
  
> [!NOTE]
> When you refresh the cache, the **Update-SPRepopulateMicroblogLMTCache** cmdlet should be run first, and then the **Update-SPRepopulateMicroblogFeedCache** cmdlet second. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ProfileServiceApplicationProxy_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> | Specifies the User Profile Service application proxy to update.  <br/>  The type must be in one of the following forms:  <br/>  A valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh  <br/>  A valid name of a service application proxy (for example, UserProfileSvcProxy1)  <br/>  An instance of a valid **SPServiceApplicationProxy** object  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ProfileServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
   
## See also

#### 

[Update-SPRepopulateMicroblogFeedCache](update-sprepopulatemicroblogfeedcache.md)

