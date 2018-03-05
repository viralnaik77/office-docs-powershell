---
title: "Get-SPTimerJob"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e2ec752d-7f04-457e-bc02-7213af5c14fe

description: "Returns timer jobs."
---

# Get-SPTimerJob

Returns timer jobs.
  
```
Get-SPTimerJob [[-Identity] <SPTimerJobPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-Type <String>] [-WebApplication <SPWebApplicationPipeBind>]
```

## Detailed Description

The **Get-SPTimerJob** cmdlet reads a specified timer job, timer jobs of a specified type, or timer jobs defined for a specified scope. If no parameters are specified, this cmdlet returns all timer job definitions for the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTimerJobPipeBind  <br/> |Specifies the timer job to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a timer job (for example, TimerJob1); or an instance of a valid **SPTimerJob** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Type** <br/> |Optional  <br/> |System.String  <br/> |Filters to return timer jobs of a specified type.  <br/> The type must be a name of a valid timer job type; for example, TimerJob1.  <br/> |
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Filters to return timer jobs defined for the scope of a specified SharePoint Web application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint Web application (for example, MyOfficeApp1); or an instance of a valid **SPWebApplication** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTimerJobPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Type** <br/> |Optional  <br/> |System.String  <br/> ||
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
   
## Errors

|**Error**|**Description**|
|:-----|:-----|
|||
   
## Exceptions

|**Exceptions**|**Description**|
|:-----|:-----|
|||
   
## Example

---------------------EXAMPLE--------------------- 
  
```
Get-SPTimerJob -WebApplication "http://servername" | select Name, DisplayName
```

This example displays all timer jobs for a specified Web application.
  
## See also

#### 

[Set-SPTimerJob](set-sptimerjob.md)
  
[Start-SPTimerJob](start-sptimerjob.md)
  
[Disable-SPTimerJob](disable-sptimerjob.md)
  
[Enable-SPTimerJob](enable-sptimerjob.md)

