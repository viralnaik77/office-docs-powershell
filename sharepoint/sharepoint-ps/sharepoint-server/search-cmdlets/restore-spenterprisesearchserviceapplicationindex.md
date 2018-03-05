---
title: "Restore-SPEnterpriseSearchServiceApplicationIndex"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 752e67bc-0f9c-47d4-bd14-e4430e5ae503

description: "Restores the search index from the specified backup files."
---

# Restore-SPEnterpriseSearchServiceApplicationIndex

Restores the search index from the specified backup files.
  
```
Restore-SPEnterpriseSearchServiceApplicationIndex -Handle <String> <COMMON PARAMETERS>

```

## Example

------------------EXAMPLE 1------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication$handle = Restore-SPEnterpriseSearchServiceApplicationIndex -SearchApplication $ssa -BackupFolder "\\sample\backup\spbr0000"Restore-SPEnterpriseSearchServiceApplicationIndex -SearchApplication $ssa -Handle $handle
```

This example starts a restore of the search index in the default search service application from a backup located at  `\\sample\backup\spbr0000`.
  
------------------EXAMPLE 2------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplicationRestore-SPEnterpriseSearchServiceApplicationIndex -SearchApplication $ssa -Handle $handle
```

This example checks the status of the running job to restore of the search index in the search service application  `Search Service Application` with the handle  `$handle` . 
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
This cmdlet will clear the complete search index for a specified search service application and replace it with the search index from the specified backup files.
  
This cmdlet supports parameter sets. The first set of parameters is for Application Configuration Attach mode and the second set of parameters is for Search Application Attach mode.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _BackupFolder_ <br/> |Required  <br/> |System.String  <br/> |Specifies the full file path of the backup files.  <br/> |
| _Handle_ <br/> |Required  <br/> |System.String  <br/> |A handle returned from an initial call using Parameter set 1.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchServiceApplication  <br/> |Specifies the search service application that contains the index files that should be restored.  <br/> |
| _AllowMove_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies a switch to move instead of copying files when restoring. Moving may be faster than copying.  <br/> |
| _AllReplicas_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies a switch to restore **all** replicas, not just the primary.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Retries_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of times to retry if temporary failure occurs.  <br/> |
| _RetryPauseSeconds_ <br/> |Optional  <br/> |System.Int32  <br/> |Seconds to pause between retries if temporary failure occurs.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchServiceApplication  <br/> ||
|**BackupFolder** <br/> |Required  <br/> |System.String  <br/> ||
|**Handle** <br/> |Required  <br/> |System.String  <br/> ||
|**AllReplicas** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AllowMove** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Retries** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**RetryPauseSeconds** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   

