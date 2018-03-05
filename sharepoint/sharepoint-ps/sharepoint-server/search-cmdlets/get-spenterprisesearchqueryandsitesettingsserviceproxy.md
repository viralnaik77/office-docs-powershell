---
title: "Get-SPEnterpriseSearchQueryAndSiteSettingsServiceProxy"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 08f5f0f9-4319-4faf-9468-7e0cd7aef9a4

description: "Returns a collection of Search service application proxies."
---

# Get-SPEnterpriseSearchQueryAndSiteSettingsServiceProxy

Returns a collection of Search service application proxies.
  
```
Get-SPEnterpriseSearchQueryAndSiteSettingsServiceProxy [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

------------------EXAMPLE------------------
  
```
$qssSvcProxy = Get-SPEnterpriseSearchQueryAndSiteSettingsServiceProxy
```

This example obtains a reference to the query and site settings service proxy.
  
## Detailed Description

The **Get-SPEnterpriseSearchQueryAndSiteSettingsServiceProxy** cmdlet reads the **SearchQueryAndSiteSettingsServiceProxy** object when a search Web service manager service is started or stopped. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   

