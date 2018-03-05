---
title: "Get-SPAppAcquisitionConfiguration"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 327ffcae-d20a-43b4-8760-375169862cf5

description: "Returns app acquisition settings."
---

# Get-SPAppAcquisitionConfiguration

Returns app acquisition settings.
  
```
Get-SPAppAcquisitionConfiguration -WebApplication <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **Get-SPAppAcquisitionConfiguration** cmdlet to return app acquisition settings from the SharePoint Store or App Catalog. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SiteSubscription** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the site collection for which app acquisition settings are to be returned.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the web application for which app acquisition settings are to be returned.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SiteSubscription** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------EXAMPLE 1-------
  
```
Get-SPAppAcquisitionConfiguration -WebApplication http://localhost
```

This example returns app acquisition settings for the specified web application.
  
------------EXAMPLE 2-------
  
```
Get-SPAppAcquisitionConfiguration -SiteSubscription http://localhost/sites/SharePointOnlineAdmin
```

This example returns app acquisition settings for the specified tenant.
  
## See also

#### 

[Set-SPAppAcquisitionConfiguration](set-spappacquisitionconfiguration.md)

