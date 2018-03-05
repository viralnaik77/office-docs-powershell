---
title: "Disable-SPAppAutoProvision"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a4ffed01-e651-434f-9ad5-b6140f349ebc

description: "Disables automatic provisioning of an app."
---

# Disable-SPAppAutoProvision

Disables automatic provisioning of an app.
  
```
Disable-SPAppAutoProvision [-AssignmentCollection <SPAssignmentCollection>] [-SiteSubscription <SPSiteSubscriptionPipeBind>]
```

## Detailed Description

Use the **Disable-SPAppAutoProvision** cmdlet to disable automatic provisioning of an app to the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the site collection for which auto provisioning is to be disabled.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
   
## Example

---------------EXAMPLE 1--------------
  
```
Disable-SPAppAutoProvision
```

This example disables app auto provisioning for the farm. The app auto provisioning is enabled by default. This setting overrides site subscription level setting.
  
---------------EXAMPLE 2--------------
  
```
$subscription = Get-SPSiteSubscription http://Contoso.com
```

```
Disable-SPAppAutoProvision -SiteSubscription $subscription
```

This example disables app auto provisioning for the site subscription for Contoso.Com site. The app auto provisioning is enabled by default.
  
## See also

#### 

[Enable-SPAppAutoProvision](enable-spappautoprovision.md)
  
[Get-SPAppAutoProvisionConnection](get-spappautoprovisionconnection.md)
  
[Set-SPAppAutoProvisionConnection](set-spappautoprovisionconnection.md)

