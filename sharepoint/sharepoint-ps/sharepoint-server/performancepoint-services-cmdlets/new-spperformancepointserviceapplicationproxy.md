---
title: "New-SPPerformancePointServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fcd8a8fa-bbc8-4f7c-9a15-58980bbc5925

description: "Creates a proxy for a PerformancePoint Service application."
---

# New-SPPerformancePointServiceApplicationProxy

Creates a proxy for a PerformancePoint Service application.
  
```
New-SPPerformancePointServiceApplicationProxy [-Name] <String> -ServiceApplication <SPPerformancePointMonitoringServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Default <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **New-SPPerformancePointServiceApplicationProxy** cmdlet creates a proxy for a PerformancePoint Service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the PerformancePoint Service application proxy to create.  <br/> The type must be a valid name of a PerformancePoint Service application proxy; for example, PerfPointAppProxy1.  <br/> |
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.PerformancePoint.Scorecards.SPPerformancePointMonitoringServiceApplicationPipeBind  <br/> |Specifies the PerformancePoint Service application that is associated with the new service application proxy.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a PerformancePoint service application (for example, PerfPointApp1); or an instance of a valid **SPPerformancePointMonitoringServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Default** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the new application proxy will be added to the default service application proxy group.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.PerformancePoint.Scorecards.SPPerformancePointMonitoringServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Default** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------------EXAMPLE--------------------
  
```
New-SPPerformancePointServiceApplicationProxy -Name PPS_Application_Proxy_01 -ServiceApplication PPS_Application_01 -Default
```

This example creates a new PerformancePoint Service application proxy named  `PPS_Application_Proxy_01`, associated with the service application named  `PPS_Application_01` and is added to the  `Default` proxy group. 
  
## See also

#### 

[Remove-SPPerformancePointServiceApplicationProxy](remove-spperformancepointserviceapplicationproxy.md)

