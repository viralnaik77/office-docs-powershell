---
title: "Get-SPInternalAppStateUpdateInterval"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 586cff56-293f-4976-b96e-0a1a5f81284c

description: "Returns the interval in hours between updates of the internal app state update job."
---

# Get-SPInternalAppStateUpdateInterval

Returns the interval in hours between updates of the internal app state update job.
  
```
Get-SPInternalAppStateUpdateInterval [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Get-SPInternalAppStateUpdateInterval** cmdlet to return the interval in hours between updates of the internal app state update job. The internal app state update job gets app upgrades from the internal app directory and sets them on app instances. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## Example

------------EXAMPLE-----------
  
```
Get-SPInternalAppStateUpdateInterval
```

This example returns the interval in hours between updates of the internal app state update job.
  
## See also

#### 

[Set-SPInternalAppStateUpdateInterval](set-spinternalappstateupdateinterval.md)

