---
title: "Get-SPAppSiteSubscriptionName"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f85b172b-5f5d-4188-8d80-fab846b4705e

description: "Returns the name of the specified site subscription."
---

# Get-SPAppSiteSubscriptionName

Returns the name of the specified site subscription.
  
```
Get-SPAppSiteSubscriptionName [-AssignmentCollection <SPAssignmentCollection>] [-SiteSubscription <SPSiteSubscriptionPipeBind>]
```

## Detailed Description

Use the **Get-SPAppSiteSubscriptionName** cmdlet to return the name of the specified site subscription. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the **SPSiteSubscription** object or the **SPSiteSubscription Id** or the URL of an **SPSite**. If this parameter is not specified, then the default site subscription is used. All SharePoint **SPSites** are members of the default site subscription if they have not been specifically assigned a site subscription.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
   
## Example

------------EXAMPLE 1-------
  
```
Get-SPAppSiteSubscriptionName
```

This example returns the name of the default site subscription.
  
------------EXAMPLE 2-------
  
```
Get-SPAppSiteSubscriptionName -SiteSubscription https://www.contoso.com
```

This example returns the name of the site subscription for SPSite https://www.contoso.com
  
## See also

#### 

[Set-SPAppSiteSubscriptionName](set-spappsitesubscriptionname.md)

