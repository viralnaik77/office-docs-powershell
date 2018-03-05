---
title: "Remove-SPPerformancePointServiceApplicationTrustedLocation"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8313c2f6-1f23-44d6-b6e2-8b67577ab76c

description: "Removes a single trusted location from a PerformancePoint Service application."
---

# Remove-SPPerformancePointServiceApplicationTrustedLocation

Removes a single trusted location from a PerformancePoint Service application.
  
```
Remove-SPPerformancePointServiceApplicationTrustedLocation -Identity <SPPerformancePointMonitoringServiceApplicationTrustedLocationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPPerformancePointServiceApplicationTrustedLocation** cmdlet deletes a single trusted location from a PerformancePoint Service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.PerformancePoint.Scorecards.SPPerformancePointMonitoringServiceApplicationTrustedLocationPipeBind  <br/> |Specifies the trusted location to delete.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid **SPPerformancePointMonitoringServiceApplicationTrustedLocation** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.PerformancePoint.Scorecards.SPPerformancePointMonitoringServiceApplicationTrustedLocationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------------EXAMPLE--------------------
  
```
Remove-SPPerformancePointServiceApplicationTrustedLocation -Identity <Valid GUID of a Trusted Location in an Application>
```

This example removes a Trusted Location having the specified GUID from a PerformancePoint Service Application.
  
## See also

#### 

[Clear-SPPerformancePointServiceApplicationTrustedLocation](clear-spperformancepointserviceapplicationtrustedlocation.md)
  
[Get-SPPerformancePointServiceApplicationTrustedLocation](get-spperformancepointserviceapplicationtrustedlocation.md)
  
[New-SPPerformancePointServiceApplicationTrustedLocation](new-spperformancepointserviceapplicationtrustedlocation.md)

