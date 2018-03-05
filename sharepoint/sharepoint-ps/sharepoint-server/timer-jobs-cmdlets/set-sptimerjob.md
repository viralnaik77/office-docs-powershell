---
title: "Set-SPTimerJob"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e40a6017-0bf0-4912-befb-3510084a0487

description: "Sets the schedule for running a timer job."
---

# Set-SPTimerJob

Sets the schedule for running a timer job.
  
```
Set-SPTimerJob [-Identity] <SPTimerJobPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Schedule <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPTimerJob** cmdlet sets the schedule for running a specified timer job. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTimerJobPipeBind  <br/> |Specifies the timer job to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a timer job (for example, TimerJob1); or an instance of a valid **SPTimerJob** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Schedule** <br/> |Required  <br/> |System.String  <br/> |Specifies the schedule for running the timer job.  <br/> The type must be a valid SharePoint Timer service (SPTimer) schedule in the form of any one of the following schedules:  <br/> - Every 5 minutes between 0 and 59  <br/> - Hourly between 0 and 59  <br/> - Daily at 15:00:00  <br/> - Weekly between Fri 22:00:00 and Sun 06:00:00  <br/> - Monthly at 15 15:00:00  <br/> - Yearly at Jan 1 15:00:00  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTimerJobPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Schedule** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Errors

|**Error**|**Description**|
|:-----|:-----|
|||
   
## Exceptions

|**Exceptions**|**Description**|
|:-----|:-----|
|||
   
## Example

-------------------EXAMPLE------------------------ 
  
```
Get-SPTimerJob job-recycle-bin-cleanup | Set-SPTimerJob -Schedule "weekly at sat 5:00"
```

This example sets the schedule to run the **job-recylce-bin-cleanup** timer job to  `weekly at sat 5:00`.
  
## See also

#### 

[Get-SPTimerJob](get-sptimerjob.md)
  
[Start-SPTimerJob](start-sptimerjob.md)
  
[Disable-SPTimerJob](disable-sptimerjob.md)
  
[Enable-SPTimerJob](enable-sptimerjob.md)

