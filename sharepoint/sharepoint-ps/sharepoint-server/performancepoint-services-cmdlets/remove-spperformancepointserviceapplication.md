---
title: "Remove-SPPerformancePointServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c39c11c1-b0d7-43bc-9744-3fbc83889489

description: "Deletes a PerformancePoint Service application from a farm."
---

# Remove-SPPerformancePointServiceApplication

Deletes a PerformancePoint Service application from a farm.
  
```
Remove-SPPerformancePointServiceApplication [-Identity] <SPPerformancePointMonitoringServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPPerformancePointServiceApplication** cmdlet deletes a PerformancePoint Service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.PerformancePoint.Scorecards.SPPerformancePointMonitoringServiceApplicationPipeBind  <br/> |Specifies the PerformancePoint Service application to delete.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a PerformancePoint Service application (for example, PerfPointApp1); or an instance of a valid **SPPerformancePointMonitoringServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.PerformancePoint.Scorecards.SPPerformancePointMonitoringServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------------EXAMPLE-----------------
  
```
Remove-SPPerformancePointServiceApplication -Identity PPSApp_01
```

This example removes the  `PPSApp_01` PerformancePoint Service application. 
  
## See also

#### 

[Get-SPPerformancePointServiceApplication](get-spperformancepointserviceapplication.md)
  
[New-SPPerformancePointServiceApplication](new-spperformancepointserviceapplication.md)
  
[Set-SPPerformancePointServiceApplication](set-spperformancepointserviceapplication.md)

