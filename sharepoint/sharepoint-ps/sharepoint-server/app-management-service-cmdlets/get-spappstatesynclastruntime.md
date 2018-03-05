---
title: "Get-SPAppStateSyncLastRunTime"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e58e8cbd-9609-4b8a-8186-3c85f76c116b

description: "Returns the latest time the app state update job was invoked."
---

# Get-SPAppStateSyncLastRunTime

Returns the latest time the app state update job was invoked.
  
```
Get-SPAppStateSyncLastRunTime [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Get-SPAppStateSyncLastRunTime** cmdlet to return the latest time the app state update job was invoked. The app state update job updates the app states in SharePoint from the marketplace including app updates. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

----------------EXAMPLE------------
  
```
Get-SPAppStateSyncLastRunTime
```

This example returns the latest time the app state update job was invoked
  

