---
title: "Get-SPBackupHistory"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc3a96db-3cc8-4991-a602-10204371047d

description: "Returns a history of backup and restore operations."
---

# Get-SPBackupHistory

Returns a history of backup and restore operations.
  
```
Get-SPBackupHistory -Directory <String> [-AssignmentCollection <SPAssignmentCollection>] [-ShowBackup <SwitchParameter>] [-ShowRestore <SwitchParameter>]
```

## Detailed Description

The **Get-SPBackupHistory** cmdlet reads a history of backup and restore operations that have been run. Specifies whether you want to display only the backup history, only the restore history, or all of the history. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Directory** <br/> |Required  <br/> |System.String  <br/> |Specifies the path where the SharePoint 2010 Products backup packages generated from a farm backup have been stored.  <br/> The type must be a valid path in either of the following forms:  <br/> - C:\folder_name  <br/> - \\server_name\folder_name  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**ShowBackup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Filters the output so that the history of backup operations only is displayed. If both the **ShowBackup** and the **ShowRestore** parameters are not specified, the history of both backup and restore operations is displayed.  <br/> |
|**ShowRestore** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Filters the output so that the history of restore operations only is displayed. If both the **ShowBackup** and the **ShowRestore** parameters are absent, the history of both backup and restore operations is displayed.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Directory** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**ShowBackup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ShowRestore** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1-----------------
  
```
Get-SPBackupHistory -Directory \\file_server\share\Backup
```

This example returns all farm backup and restore operations that have been run for the  _\\file_server\share\Backup_ directory. 
  
------------------EXAMPLE 2-----------------
  
```
Get-SPBackupHistory -Directory C:\Backup -ShowBackup
```

This example returns all of the farm backup operations that have been run for the  _C:\Backup_ directory. 
  
------------------EXAMPLE 3-----------------
  
```
(Get-SPBackupHistory -Directory C:\Backup -ShowBackup)[0].SelfId | Restore-SPFarm -Directory C:\Backup -RestoreMethod overwrite
```

This example gets all of the farm backup operations that have been run for the  _C:\Backup_ directory, finds the most recent backup, and then passes its backup GUID to the **Restore-SPFarm** cmdlet. The **Restore-SPFarm** cmdlet will then perform an overwrite restore from that backup package. 
  
## See also

#### 

[Backup-SPFarm](backup-spfarm.md)
  
[Backup-SPConfigurationDatabase](backup-spconfigurationdatabase.md)
  
[Restore-SPFarm](restore-spfarm.md)

