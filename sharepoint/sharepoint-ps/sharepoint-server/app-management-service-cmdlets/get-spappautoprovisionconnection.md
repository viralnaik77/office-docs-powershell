---
title: "Get-SPAppAutoProvisionConnection"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9be8576c-c1f2-4c22-96bb-ce6968d04597

description: "Returns provision connection settings for an app."
---

# Get-SPAppAutoProvisionConnection

Returns provision connection settings for an app.
  
```
Get-SPAppAutoProvisionConnection [-AssignmentCollection <SPAssignmentCollection>] [-ConnectionType <RemoteWebHost>] [-SiteSubscription <SPSiteSubscriptionPipeBind>]
```

## Detailed Description

Use the **Get-SPAppAutoProvisionConnection** cmdlet to return the provision connection settings for an app. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**ConnectionType** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPAppCmdlets.GetAppAutoProvisionCmdlet+ConnectionTypes  <br/> |Specifies the connection type to provision the app.  <br/> |
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the site collection from which to return the provision connection.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**ConnectionType** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPAppCmdlets.GetAppAutoProvisionCmdlet+ConnectionTypes  <br/> ||
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
   
## Example

---------------EXAMPLE 1----------
  
```
Get-SpAppAutoProvisionConnection
```

This example returns the entire app auto provisioning connection information for the default site subscription.
  
---------------EXAMPLE 2----------
  
```
$subscription = Get-SPSiteSubscription http://Contoso.com
```

```
Get-SPAppAutoProvisionConnection -SiteSubscription $subscription -ConnectionType RemoteWebHost
```

This example returns the remote web host app auto provisioning connection information for the site subscription for Contoso.com site
  
## See also

#### 

[Set-SPAppAutoProvisionConnection](set-spappautoprovisionconnection.md)

