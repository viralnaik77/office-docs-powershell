---
title: "Backup and recovery cmdlets in SharePoint Server 2016"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 2/25/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: 2ec8e3d1-f9f7-45b7-980a-d3c19d726d33
description: "Summary: Lists Windows PowerShell cmdlets that help you complete backup and recovery operation in SharePoint Server 2016."
---

# Backup and recovery cmdlets in SharePoint Server 2016

 **Summary:** Lists Windows PowerShell cmdlets that help you complete backup and recovery operation in SharePoint Server 2016. 
  
A backup is a copy of data that is used to restore and recover that data after a system failure. Maintaining backups of data is useful for routine purposes, such as copying a database from one server to another, setting up database mirroring, archiving for governmental purposes, and disaster recovery.
  
In SharePoint Server 2016, you can use Microsoft PowerShell functionality to perform a backup or restore process for the following items:
  
- Farm
    
- Site collection
    
- Configuration database
    
- Services
    
- List or document
    
[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md) includes a complete list of all cmdlets in SharePoint Server 2016. 
  
|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Backup-SPConfigurationDatabase](backup-spconfigurationdatabase.md)** <br/> |Performs a farm-level configuration-only backup.  <br/> |
|**[Backup-SPFarm](backup-spfarm.md)** <br/> |Creates a backup of an individual database, Web application, or the entire farm.  <br/> |
|**[Restore-SPFarm](restore-spfarm.md)** <br/> |Restores one or more items from a backup.  <br/> |
|**[Backup-SPSite](backup-spsite.md)** <br/> |Performs a backup of a site collection.  <br/> |
|**[Restore-SPSite](restore-spsite.md)** <br/> |Restores a site collection.  <br/> |
|**[Get-SPBackupHistory](get-spbackuphistory.md)** <br/> |Returns a history of backup and restore operations.  <br/> |
   
## See also

#### 

[Microsoft PowerShell for SharePoint Server reference](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/microsoft-powershell-for-sharepoint-server-reference.md)

