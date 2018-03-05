---
title: "Get-SPEnterpriseSearchVssDataPath"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 26d6e44c-a606-47a1-a3e0-c4919670f684
description: "Retrieves the index paths for all active search index components on the current server."
---

# Get-SPEnterpriseSearchVssDataPath

Retrieves the index paths for all active search index components on the current server.
  
```
Get-SPEnterpriseSearchVssDataPath [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

------------------EXAMPLE-----------------
  
```
Get-SPEnterpriseSearchVssDataPath
```

This example gets the index paths for all active index components on the current server.
  
## Detailed Description

This cmdlet retrieves the index paths for all active index components on the current server. This list is required as input by the Search VSS Writer in order to perform VSS backup of the current server. This cmdlet will typically be called from a VSS script, and rarely used directly.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   

