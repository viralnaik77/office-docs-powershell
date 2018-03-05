---
title: "Update-SPMicrofeedOptions"
ms.author: kirks
author: Techwriter40
ms.date: 3/1/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 58ffa82b-2472-4927-b355-c823d71b01b9

description: "Updates the feed cache settings for the current user profile application."
---

# Update-SPMicrofeedOptions

Updates the feed cache settings for the current user profile application.
  
```
Update-SPMicrofeedOptions -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-AsyncRefs <$true | $false>] [-MaxCacheMs <Int32>] [-MaxMentions <Int32>] [-MaxPostLength <Int32>] [-MaxTags <Int32>] [-SiteSubscription <SPSiteSubscriptionPipeBind>]

```

## Example

--------------EXAMPLE------------
  
```
Update-SPMicrofeedOptions -ProfileServiceApplicationProxy c6681d53-e6c4-432f-9f31-22d3de81b00c
```

This example updates settings from the specified User Profile Service Application Proxy.
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ProfileServiceApplicationProxy_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the unique identifier for the proxy.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _AsyncRefs_ <br/> |Optional  <br/> |System.Boolean  <br/> |Performs reference-posts via async threads.  <br/> If the value is set to True, each @mention in a thread is handled in its own .NET threadpool async tthread.  <br/> |
| _MaxCacheMs_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the permissible range of cache loop up time.  <br/> |
| _MaxMentions_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number @mentions per post and reply.  <br/> |
| _MaxPostLength_ <br/> |Optional  <br/> |System.Int32  <br/> |Sets the maximum number of characters in a Microfeed post.  <br/> |
| _MaxTags_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number #tags per post and reply.  <br/> |
| _SiteSubscription_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the account under which this service should run. This parameter is mandatory in a hosted-environment and optional in a non-hosted environment.  <br/> |
   
## See also

#### 

[Get-SPMicrofeedOptions](get-spmicrofeedoptions.md)

