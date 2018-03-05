---
title: "Get-SPPerformancePointServiceApplicationTrustedLocation"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6106dec2-42e1-4210-8a38-dadc03a5dfcf

description: "Returns a trusted location object and properties for a PerformancePoint Service application."
---

# Get-SPPerformancePointServiceApplicationTrustedLocation

Returns a trusted location object and properties for a PerformancePoint Service application.
  
```
Get-SPPerformancePointServiceApplicationTrustedLocation [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Identity <SPPerformancePointMonitoringServiceApplicationTrustedLocationPipeBind>] [-ServiceApplication <SPPerformancePointMonitoringServiceApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Get-SPPerformancePointMonitoringServiceApplicationTrustedLocation** cmdlet to read a trusted location object and properties. If the **Identity** parameter is not specified, this cmdlet returns the list of all trusted locations and their properties for a PerformancePoint Service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Identity** <br/> |Optional  <br/> |Microsoft.PerformancePoint.Scorecards.SPPerformancePointMonitoringServiceApplicationTrustedLocationPipeBind  <br/> |Specifies the trusted location to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid **SPPerformancePointMonitoringServiceApplicationTrustedLocation** object.  <br/> |
|**ServiceApplication** <br/> |Optional  <br/> |Microsoft.PerformancePoint.Scorecards.SPPerformancePointMonitoringServiceApplicationPipeBind  <br/> |Specifies the PerformancePoint Service application that contains the trusted location.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a PerformancePoint Service application (for example, PerfPointApp1); or an instance of a valid **SPPerformancePointMonitoringServiceApplication** object.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Identity** <br/> |Optional  <br/> |Microsoft.PerformancePoint.Scorecards.SPPerformancePointMonitoringServiceApplicationTrustedLocationPipeBind  <br/> ||
|**ServiceApplication** <br/> |Optional  <br/> |Microsoft.PerformancePoint.Scorecards.SPPerformancePointMonitoringServiceApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

----------------------EXAMPLE---------------------- 
  
```
Get-SPPerformancePointServiceApplication PPSApp_01 | Get-SPPerformancePointServiceApplicationTrustedLocation -Identity $_.ID | select *
```

This example retrieves  `TrustedLocation` information for the  `PPSApp_01` PerformancePoint Service application. 
  
## See also

#### 

[Clear-SPPerformancePointServiceApplicationTrustedLocation](clear-spperformancepointserviceapplicationtrustedlocation.md)
  
[New-SPPerformancePointServiceApplicationTrustedLocation](new-spperformancepointserviceapplicationtrustedlocation.md)
  
[Remove-SPPerformancePointServiceApplicationTrustedLocation](remove-spperformancepointserviceapplicationtrustedlocation.md)

