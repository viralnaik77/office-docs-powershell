---
title: "Start-SPAdminJob"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a96146cd-9973-4680-9a0b-d91ec51200d5

description: "Immediately starts any waiting administrative job on the local computer."
---

# Start-SPAdminJob

Immediately starts any waiting administrative job on the local computer.
  
```
Start-SPAdminJob [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Start-SPAdminJob** cmdlet to execute all administrative timer jobs immediately rather than waiting for the timer job to run. 
  
When the service account for the SharePoint 2010 Administration service (SPAdminV4)) is disabled (necessary in some installations for security reasons), the **Start-SPAdminJob** cmdlet must be run on all computers to perform administrative task like provisioning. 
  
When you run this cmdlet in person (not in script), use the **Verbose** parameter to see the individual administrative operations that are run. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Return Types

none
  
## Errors

|**Error**|**Description**|
|:-----|:-----|
|||
   
## Exceptions

|**Exceptions**|**Description**|
|:-----|:-----|
|||
   
## Example

------------------EXAMPLE-----------------------
  
```
Start-SPAdminJob -Verbose
```

This example runs all waiting administrative jobs and shows verbose output to the administrator.
  
## See also

#### 

[Get-SPTimerJob](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/timer-jobs-cmdlets/get-sptimerjob.md)
  
[Set-SPTimerJob](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/timer-jobs-cmdlets/set-sptimerjob.md)
  
[Enable-SPTimerJob](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/timer-jobs-cmdlets/enable-sptimerjob.md)
  
[Disable-SPTimerJob](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/timer-jobs-cmdlets/disable-sptimerjob.md)

