---
title: "New-SPSiteSubscription"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 134f4d1a-28c0-4239-9e6e-4e886f877f1b

description: "Creates a new site subscription."
---

# New-SPSiteSubscription

Creates a new site subscription.
  
```
New-SPSiteSubscription [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **New-SPSiteSubscription** cmdlet creates a new subscription to which the SPSites object can belong. Sites that are members of a site subscription can share settings and configuration information. A site collection can be a member of only one site subscription and, once set, cannot be changed. 
  
Site subscriptions are not persisted in a database until used in conjunction with either an SPSite or the Site Subscription Settings Service. After a site subscription is applied to any site collection in the farm, the site subscription can be retrieved by using the **Get-SPSiteSubscription** cmdlet. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## Example

------------------EXAMPLE 1-----------------------
  
```
New-SPSiteSubscription |%{ New-SPSite http://contoso.com/sites/admin -SiteSubscription $_ -Template "TenantAdmin#0"}
```

```

```

This example creates a new site subscription and applies it to a new Tenant Administration site collection.
  
------------------EXAMPLE 2-----------------------
  
```
$s = New-SPSiteSubscription
```

```
Get-SPSite http://sitename | Set-SPSite -SiteSubscription $s
```

```
Set-SPSite http://sitename -SiteSubscription {New-SPSiteSubscription}
```

This example adds a new subscription to an existing site collection at  `http://sitename`.
  
## See also

#### 

[Get-SPSiteSubscription](get-spsitesubscription.md)
  
[Remove-SPSiteSubscription](remove-spsitesubscription.md)

