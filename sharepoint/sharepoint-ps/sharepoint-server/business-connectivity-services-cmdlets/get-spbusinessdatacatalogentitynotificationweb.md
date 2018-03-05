---
title: "Get-SPBusinessDataCatalogEntityNotificationWeb"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e4d3094c-d18d-4cde-bad4-c4bc29898e50

description: "Returns the entity notification site."
---

# Get-SPBusinessDataCatalogEntityNotificationWeb

Returns the entity notification site.
  
```
Get-SPBusinessDataCatalogEntityNotificationWeb -ServiceContext <SPServiceContextPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Get-SPBusinessDataCatalogEntityNotificationWeb** cmdlet to return the entity notification site that can receive and forward external system notifications. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context for which the entity notification web has to be returned.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-------EXAMPLE-----------
  
```
Get-SPBusinessDataCatalogEntityNotificationWeb -ServiceContext "http://contoso"
```

This example returns the entity notification site for the site collection at http://contoso.
  
## See also

#### 

[Clear-SPBusinessDataCatalogEntityNotificationWeb](clear-spbusinessdatacatalogentitynotificationweb.md)
  
[Set-SPBusinessDataCatalogEntityNotificationWeb](set-spbusinessdatacatalogentitynotificationweb.md)

