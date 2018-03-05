---
title: "Backup-SPEnterpriseSearchServiceApplicationIndex"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 2/18/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 625bd9f3-d7f5-4d8a-9edf-6cb270ce27b3

description: "Applies to: UNRESOLVED_TOKEN_VAL(zzpub_appliesTo)"
---

# Backup-SPEnterpriseSearchServiceApplicationIndex

 * **Applies to: ** UNRESOLVED_TOKEN_VAL(zzpub_appliesTo) * 
  
Takes a backup of the search index to a specified backup location.
  
```
Backup-SPEnterpriseSearchServiceApplicationIndex -BackupFolder <String> -Phase <Int32> <COMMON PARAMETERS>

```

## Example

------------------EXAMPLE 1------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
Backup-SPEnterpriseSearchServiceApplicationIndex -Phase 1 -SearchApplication $ssa -BackupFolder "\\backuphost\backupfolder" -BackupHandleFile "\\backuphost\backupfolder\backuphandle.txt" -Retries 3
```

This example starts a  `Phase 1` backup of the search index for the default search application, and stores the backup at the location  `\\backuphost\backupfolder`. The cmdlet stores a handle file  `backuphandle.txt` that is used by the second phase cmdlet. 
  
------------------EXAMPLE 2------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
Backup-SPEnterpriseSearchServiceApplicationIndex -Phase 1 $ssa -BackupFolder "\\backuphost\backupfolder" -BackupHandleFile "\\backuphost\backupfolder\backuphandle.txt" -Retries 3
```

This example checks the backup status and progress by re-running the cmdlet for Phase 1.
  
------------------EXAMPLE 3------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
Backup-SPEnterpriseSearchServiceApplicationIndex -Phase 2 -SearchApplication $ssa -BackupFolder "\\backuphost\backupfolder" -BackupHandleFile "\\backuphost\backupfolder\backuphandle.txt" -Retries 3
```

This example starts the Phase 2 of the search index backup by using the same backup location and backup handle file as used for Phase 1. The Search Service Application must be paused before the second phase can be started. 
  
## Detailed Description

This cmdlet will take a backup of the search index to a specified backup location. The cmdlet has to be run in two phases. Phase one will take a backup of what is present in the index at the time that the backup cmdlet is run. Phase two will take a differential backup of what was added to the index after you started the first phase index backup.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Abort_ <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Aborts an ongoing backup job using the file handle located in BackupHandleFile.  <br/> |
| _BackupFolder_ <br/> |Required  <br/> |System.String  <br/> |Full UNC path of the backup files should be written.  <br/> |
| _BackupHandleFile_ <br/> |Required  <br/> |System.String  <br/> |Specifies a file handle for an ongoing backup job.  <br/> |
| _Phase_ <br/> |Required  <br/> |System.Int32  <br/> |Specifies the phase of the backup job.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchServiceApplication  <br/> |Name of the search service application to be backed up  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _PeerToPeer_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |This parameter is not intended for IT Professionals, it only applies to SharePoint Online.  <br/> |
| _Retries_ <br/> |Optional  <br/> |System.Int32  <br/> |Number of times to retry if temporary failure occurs.  <br/> |
| _SpecifiedBackupHandle_ <br/> |Optional  <br/> |System.String  <br/> |This parameter is not intended for IT Professionals, it only applies to SharePoint Online.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Abort** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Phase** <br/> |Required  <br/> |System.Int32  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchServiceApplication  <br/> ||
|**BackupFolder** <br/> |Required  <br/> |System.String  <br/> ||
|**BackupHandleFile** <br/> |Required  <br/> |System.String  <br/> ||
|**Retries** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   

