---
title: "Get-SPMicrofeedOptions"
ms.author: kirks
author: Techwriter40
ms.date: 2/25/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b79a40a3-aed0-46a2-a5d5-ceb9ce7686cb

description: "Returns the feed cache settings for the current user profile application."
---

# Get-SPMicrofeedOptions

Returns the feed cache settings for the current user profile application.
  
```
Get-SPMicrofeedOptions -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-SiteSubscription <SPSiteSubscriptionPipeBind>]

```

## Example

--------------EXAMPLE------------
  
```
Get-SPMicrofeedOptions -ProfileServiceApplicationProxy c6681d53-e6c4-432f-9f31-22d3de81b00c
```

This example returns cache feed settings from the specified User Profile Service Application Proxy.
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ProfileServiceApplicationProxy_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the unique identifier for the proxy.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _SiteSubscription_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the account under which this service should run. This parameter is mandatory in a hosted-environment and optional in a non-hosted environment.  <br/> |
   
## See also

#### 

[Update-SPMicrofeedOptions](update-spmicrofeedoptions.md)

