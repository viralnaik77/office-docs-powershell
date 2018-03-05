---
title: "Get-SPSiteSubscription"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d79fb60b-ba72-4187-bcb3-152d22368f71

description: "Returns the site subscription for the given URL or all site subscriptions in the local farm."
---

# Get-SPSiteSubscription

Returns the site subscription for the given URL or all site subscriptions in the local farm.
  
```
Get-SPSiteSubscription [[-Identity] <SPSiteSubscriptionPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPSiteSubscription** cmdlet returns the site subscription for the given URL when the **Identity** parameter is used. If no parameter is specified, all unique site subscriptions in the farm are listed. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the ID of the subscription.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Default** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies the default site subscription. Any site created without specifying a site subscription ID will be part of the default.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------------EXAMPLE----------------------
  
```
$SiteSub = Get-SPSiteSubscription http://Contoso.com
```

```
$SiteSub = Get-SPSite http://contoso.com | Get-SPSiteSubscription
```

This example retrieves the site subscription for  `http://Contoso.com`.
  
## See also

#### 

[New-SPSiteSubscription](new-spsitesubscription.md)
  
[Remove-SPSiteSubscription](remove-spsitesubscription.md)

