---
title: "Start-SPContentDeploymentJob"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d34e88ba-1f37-4611-92c8-1e67b41c5923

description: "Starts a content deployment job."
---

# Start-SPContentDeploymentJob

Starts a content deployment job.
  
```
Start-SPContentDeploymentJob -Identity <SPContentDeploymentJobPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DeploySinceTime <String>] [-TestEnabled <SwitchParameter>] [-UseSpecificSnapshot <String>] [-WaitEnabled <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------------EXAMPLE-----------------
  
```
Get-SPContentDeploymentPath "Path 1" | New-SPContentDeploymentJob -Name "Job 1" -SPContentDeploymentPath $_ -IncrementalEnabled:$true -ScheduleEnabled:$false | Start-SPContentDeploymentJob
```

This example creates a content deployment job  `Job 1` and runs it immediately. 
  
## Detailed Description

The **Start-SPContentDeploymentJob** cmdlet starts a content deployment job. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.Publishing.Cmdlet.SPContentDeploymentJobPipeBind  <br/> |Specifies the content deployment job to run.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a content deployment job (for example, DeployJob1); or an instance of a valid **SPContentDeploymentJob** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DeploySinceTime_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the date to use to determine what changes to export incrementally. This parameter is ignored if the deployment job type is full.  <br/> The type must be a valid DateTime type, in the form 2010,12,05.  <br/> |
| _TestEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Runs the content deployment job in test mode only.  <br/> |
| _UseSpecificSnapshot_ <br/> |Optional  <br/> |System.String  <br/> |PARAMVALUE: String  <br/> |
| _WaitEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the command is not returned until the operation is complete.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Publishing.Cmdlet.SPContentDeploymentJobPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DeploySinceTime** <br/> |Optional  <br/> |System.String  <br/> ||
|**TestEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**UseSpecificSnapshot** <br/> |Optional  <br/> |System.String  <br/> ||
|**WaitEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPContentDeploymentJob](get-spcontentdeploymentjob.md)
  
[New-SPContentDeploymentJob](new-spcontentdeploymentjob.md)
  
[Remove-SPContentDeploymentJob](remove-spcontentdeploymentjob.md)
  
[Set-SPContentDeploymentJob](set-spcontentdeploymentjob.md)

