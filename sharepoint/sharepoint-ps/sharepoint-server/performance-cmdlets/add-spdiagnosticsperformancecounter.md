---
title: "Add-SPDiagnosticsPerformanceCounter"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69742248-7a79-403d-8617-b0524cb5c9a0

description: "Adds a new instance of a performance counter to a Web front end computer or a database server."
---

# Add-SPDiagnosticsPerformanceCounter

Adds a new instance of a performance counter to a Web front end computer or a database server.
  
```
Add-SPDiagnosticsPerformanceCounter -Category <String> -Counter <String> [-AllInstances <SwitchParameter>] [-DatabaseServer <SwitchParameter>] [-WebFrontEnd <SwitchParameter>] <COMMON PARAMETERS>

```

## Example

------------------EXAMPLE 1------------------
  
```
Add-SPDiagnosticsPerformanceCounter -category ASP.NET -Counter "Requests Queued"
```

This example adds the counter that has the name  `ASP.NET\Requests Queued` on front end Web servers. 
  
------------------EXAMPLE 2------------------
  
```
Add-SPDiagnosticsPerformanceCounter -category PhysicalDisk -counter "Avg. Disk Queue Length" -allinstances
```

This example adds all instances of the counter  `PhysicalDisk` in the category  `Avg. Disk Queue Length` on front end Web servers. 
  
------------------EXAMPLE 3------------------
  
```
Add-SPDiagnosticsPerformanceCounter -category Processor -counter "% Processor Time" -instance "_Total" -databaseserver
```

This example adds the  `_Total` instance of the counter  `% Processor Time` in the category  `Processor` on database servers. 
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
The **Add-SPDiagnosticsPerformanceCounter** cmdlet adds a performance counter to a front end Web server or a database server. A performance counter is read and recorded in the usage database. By default, the new performance counter is added to the database servers in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Category_ <br/> |Required  <br/> |System.String  <br/> |Specifies the category of performance counter to add to the target Web front end computer or database server.  <br/> The type must be a valid name of a category of performance counters; for example, ASP.NET, PhysicalDisk, or Processor.  <br/> |
| _Counter_ <br/> |Required  <br/> |System.String  <br/> |Specifies the type of counter to add to the target Web front end computer or database server.  <br/> The type must be a valid name of counter type; for example, Requests Queued, Avg. Disk Queue Length, and % Processor Time.  <br/> |
| _CounterList_ <br/> |Required  <br/> |System.String[]  <br/> |Specifies the list of counters to add to the database server.  <br/> |
| _Instance_ <br/> |Required  <br/> |System.String  <br/> |Specifies the display name of the new performance counter.  <br/> The type must be a valid name of a performance counter instance; for example Total_PerfCounter.  <br/> |
| _AllInstances_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Collects all instances of a counter category and type on the target Web front end computer or database server.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Adds the specified performance counter to all database servers in the farm.  <br/> |
| _WebFrontEnd_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Adds the specified performance counter to all Web front end computers in the farm.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Category** <br/> |Required  <br/> |System.String  <br/> ||
|**Counter** <br/> |Required  <br/> |System.String  <br/> ||
|**Instance** <br/> |Required  <br/> |System.String  <br/> ||
|**AllInstances** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WebFrontEnd** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPDiagnosticsPerformanceCounter](get-spdiagnosticsperformancecounter.md)
  
[Remove-SPDiagnosticsPerformanceCounter](remove-spdiagnosticsperformancecounter.md)

