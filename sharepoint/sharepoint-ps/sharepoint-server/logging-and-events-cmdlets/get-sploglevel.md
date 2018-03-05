---
title: "Get-SPLogLevel"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1bb57b3d-8bf3-4fb2-8ef2-dd3eafe3a899

description: "Returns a list of objects or diagnostic levels."
---

# Get-SPLogLevel

Returns a list of objects or diagnostic levels.
  
```
Get-SPLogLevel [-AssignmentCollection <SPAssignmentCollection>] [-Identity <String[]>]
```

## Detailed Description

The **Get-SPLogLevel** cmdlet displays a list of objects or diagnostic levels based on the criteria specified. If no parameter is specified, a list of all diagnostic levels for all categories is returned. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Identity** <br/> |Optional  <br/> |System.String[]  <br/> |Specifies a valid category name; for example, Backup and Restore, or Administration.  <br/> |
   
## Example

--------------EXAMPLE 1-----------------
  
```
Get-SPLogLevel
```

This example displays throttle levels for all categories.
  
--------------EXAMPLE 2-----------------
  
```
Get-SPLogLevel -Identity "Category1"
```

This example displays the throttle level for the  `Category1` category. 
  
--------------EXAMPLE 3-----------------
  
```
"Cat1", "Cat2", "Cat3" | Get-SpLogLevel
```

This example displays the throttle level for multiple categories.
  
--------------EXAMPLE 4-----------------
  
```
Get-SPLogLevel -Identity "Area:*"
```

This example displays the throttle level for all categories in one area.
  
## See also

#### 

[Set-SPLogLevel](set-sploglevel.md)
  
[Clear-SPLogLevel](clear-sploglevel.md)

