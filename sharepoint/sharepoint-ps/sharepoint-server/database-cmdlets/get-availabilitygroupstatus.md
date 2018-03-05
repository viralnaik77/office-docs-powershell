---
title: "Get-AvailabilityGroupStatus"
ms.author: kirks
author: Techwriter40
ms.date: 2/10/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa27429-6852-4da0-bb5e-a037f8dbead0

description: "Returns one or more objects representing the availability groups known to the SharePoint farm."
---

# Get-AvailabilityGroupStatus

Returns one or more objects representing the availability groups known to the SharePoint farm.
  
```
Get-AvailabilityGroupStatus [-AssignmentCollection <SPAssignmentCollection>] [-Identity <String>]

```

## Example

--------------EXAMPLE----------- 
  
```
Get-AvailabilityGroupStatus -Identity MyAvailabilityGroup 
```

This example returns an availability group named "MyAvailabilityGroup".
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |System.String  <br/> |Finds the availability group whose name property matches this string. Otherwise, returns all availability groups.  <br/> |
   
## See also

#### 

[Add-DatabaseToAvailabilityGroup](add-databasetoavailabilitygroup.md)
  
[Remove-DatabaseFromAvailabilityGroup](remove-databasefromavailabilitygroup.md)

