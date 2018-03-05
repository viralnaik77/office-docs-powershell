---
title: "Get-SPServiceContext"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 73bde07b-ac29-4f76-874a-623471a6bdeb

description: "Returns a service context."
---

# Get-SPServiceContext

Returns a service context.
  
```
Get-SPServiceContext [-Site] <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Get-SPServiceContext** cmdlet returns a service context or a collection of service contexts. Specify the **Site** parameter to return an individual service context, or specify the **SiteSubscription** parameter to return a collection of service contexts. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Returns the service context for only the Web application that contains the specified site collection.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL, in the form http://server_name; or an instance of a valid **SPSite** object.  <br/> |
|**SiteSubscription** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Returns all of the service contexts for all Web applications in which the specified site subscription has site collections.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a site subscription (for example, SiteSubscriptionConfig1); or an instance of a valid **SiteSubscription** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**SiteSubscription** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

----------------EXAMPLE---------------
  
```
$sitesub = Get-SPSiteSubscription http://my.contoso.com/
```

```
Get-SPServiceContext $sitesub
```

This example returns the service context for a site in a hosted environment.
  

