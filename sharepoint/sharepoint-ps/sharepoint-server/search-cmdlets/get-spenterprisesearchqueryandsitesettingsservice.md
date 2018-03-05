---
title: "Get-SPEnterpriseSearchQueryAndSiteSettingsService"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 245a4b7a-98d7-4fa0-a99a-ebb3c4be821b

description: "Returns the search manager service."
---

# Get-SPEnterpriseSearchQueryAndSiteSettingsService

Returns the search manager service.
  
```
Get-SPEnterpriseSearchQueryAndSiteSettingsService [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

------------------EXAMPLE------------------
  
```
$qssService = Get-SPEnterpriseSearchQUeryAndSiteSettingsService
```

This example obtains a reference to the query and site settings service.
  
## Detailed Description

The **Get-SPEnterpriseSearchQueryAndSiteSettingsService** cmdlet returns a manager service. A manager service is the endpoint for the search service application to process queries and site administration requests from the search service application proxy. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   

