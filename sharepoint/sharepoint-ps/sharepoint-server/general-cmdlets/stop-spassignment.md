---
title: "Stop-SPAssignment"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/20/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b99949ef-6d60-4a4f-9031-723bcb7e0468

description: "Disposes of objects in the provided assignment collection."
---

# Stop-SPAssignment

Disposes of objects in the provided assignment collection.
  
```
Stop-SPAssignment [[-SemiGlobal] <SPAssignmentCollection>] [-AssignmentCollection <SPAssignmentCollection>] [-Global <SwitchParameter>]
```

## Detailed Description

The **Stop-SPAssignment** cmdlet disposes of objects in the provided assignment collection. Use the **Global** parameter to dispose of all objects in the global assignment collector and to stop the global store from collecting additional objects. Provide a **SemiGlobal** assignment collector to dispose of all contained objects. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SemiGlobal** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentColletion  <br/> |Provides the assignment collector from which to dispose of objects.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Global** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Stops the global assignment collector from storing objects, and disposes of any objects contained by the global assignment collector.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SemiGlobal** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Global** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Start-SPAssignment -global
```

```
$w=Get-SPWeb http://MyWeb
```

```
$w | Set-SPWeb -title "Accounting"
```

```
Stop-SPAssignment -global
```

This example uses simple assignment. While easier to use simple assignment, running commands that iterate through multiple **SPSite** or **SPWeb** objects while simple assignment is enabled is not recommended. Ensure that **Stop-SPAssignment** is run before attempting any iterations of multiple objects. 
  
## See also

#### 

[Start-SPAssignment](start-spassignment.md)

