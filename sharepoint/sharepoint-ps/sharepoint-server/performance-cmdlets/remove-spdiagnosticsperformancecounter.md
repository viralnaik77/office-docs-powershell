---
title: "Remove-SPDiagnosticsPerformanceCounter"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40850069-75f2-48e4-ad35-d12a940eddb1

description: "Removes an instance of a performance counter."
---

# Remove-SPDiagnosticsPerformanceCounter

Removes an instance of a performance counter.
  
```
Remove-SPDiagnosticsPerformanceCounter [-Category] <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Counter <String>] [-DatabaseServer <SwitchParameter>] [-Instance <String>] [-WebFrontEnd <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPDiagnosticsPerformanceCounter** cmdlet removes performance counters from the collection of performance counters that are read and recorded in the usage database. This cmdlet can also be used to remove entire categories and types of counters from the collection. If either the **DatabaseServer** or **WebFrontEnd** parameters are not specified, this cmdlet removes the specified performance counters on the front end Web servers in the farm. 
  
> [!NOTE]
> The **Remove-SPDiagnosticsPerformanceCounter** cmdlet is only available by using Microsoft PowerShell. There is no user interface. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Category** <br/> |Required  <br/> |System.String  <br/> |Specifies the category of performance counters to remove.  <br/> The type must be a valid name of a category of performance counters; for example, ASP.NET, PhysicalDisk, or Processor.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Counter** <br/> |Optional  <br/> |System.String  <br/> |Specifies the type of counter to remove. If this parameter is not specified, this cmdlet removes all performance counters of the specified category.  <br/> The type must be a valid name of counter type; for example, Requests Queued, Avg. Disk Queue Length, and % Processor Time.  <br/> |
|**DatabaseServer** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Removes the specified performance counters that are collected on the database servers in the farm.  <br/> |
|**Instance** <br/> |Optional  <br/> |System.String  <br/> |Specifies the instance name of the performance counter to remove. If this parameter is not specified, this cmdlet removes all instances of the specified performance counter.  <br/> The type must be a valid name of a performance counter instance; for example Total_PerfCounter.  <br/> |
|**WebFrontEnd** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Removes performance counters that are collected on the front end Web servers in the farm.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

------------------EXAMPLE 1------------------
  
```
Remove-SPDiagnosticsPerformanceCounter -category ASP.NET
```

This example removes all the counters in the category  `ASP.NET` on front end Web servers. 
  
------------------EXAMPLE 2------------------
  
```
Remove-SPDiagnosticsPerformanceCounter -category ASP.NET -Counter "Requests Queued"
```

This example removes the counters in the category  `ASP.NET` that have requests queued on front end Web servers. 
  
------------------EXAMPLE 3------------------
  
```
Remove-SPDiagnosticsPerformanceCounter -category Processor -counter "% Processor Time" -instance "_Total" -databaseserver
```

This example removes the counters of the  `_Total` instance, with the counter  `% Processor Time` in the category  `Processor` on database servers. 
  
## See also

#### 

[Add-SPDiagnosticsPerformanceCounter](add-spdiagnosticsperformancecounter.md)
  
[Get-SPDiagnosticsPerformanceCounter](get-spdiagnosticsperformancecounter.md)

