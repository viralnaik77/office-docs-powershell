---
title: "Backup-SPSite"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d4c31a1a-82a7-425f-b1bb-22e70bedd338

description: "Performs a backup of a site collection."
---

# Backup-SPSite

Performs a backup of a site collection.
  
```
Backup-SPSite -Identity <SPSitePipeBind> -Path <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-NoSiteLock <SwitchParameter>] [-UseABSDocStreamInfo <SwitchParameter>] [-UseSqlSnapshot <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

-------------------EXAMPLE 1--------------------
  
```
Backup-SPSite http://server_name/sites/site_name -Path C:\Backup\site_name.bak
```

This example backs up a site collection at http://server_name/sites/site_name to the C:\Backup\site_name.bak file.
  
-------------------EXAMPLE 2--------------------
  
```
Get-SPSiteAdministration http://server_name/sites/site_name | Backup-SPSite -Path C:\Backup\site_name.bak
```

This example backs up a site collection at http://server_name/sites/site_name to the C:\Backup\site_name.bak file. Same result as Example 1, but a different way of performing the operation.
  
-------------------EXAMPLE 3--------------------
  
```
Backup-SPSite http://server_name/sites/site_name -Path C:\Backup\site_name.bak -UseSqlSnapshot
```

This example backs up a site collection using database snapshots to ensure backup integrity.
  
## Detailed Description

The **Backup-SPSite** cmdlet performs a backup of the site collection when the **Identity** parameter is used. 
  
By default, the site collection will be set to read-only for the duration of the backup to reduce the potential for user activity during the backup operation to corrupt the backup. If you have SQL Server Enterprise Edition, we recommend that **UseSqlSnapshot** parameter be used because this ensures a valid backup while it allows users to continue reading and writing to the site collection during the backup. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the URL or GUID of the site collection to be backed up.  <br/> For example, a valid URL, such as http://server_name/sites/site_name or a GUID such as, "01234567-89ab-cdef-0123-456789abcdef"  <br/> |
| _Path_ <br/> |Required  <br/> |System.String  <br/> |Specifies the full path to the backup file (that is, C:\Backup\site_name.bak.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Force_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specify to overwrite an existing backup file if it already exists.  <br/> |
| _NoSiteLock_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies the site collection to remain read and write during the backup.  <br/> If the **NoSiteLock** parameter is not specified, then a site collection that has a site collection lock setting of "none" or "no additions" will be temporarily set to "read only" while the site collection backup is performed. Once the backup has completed, the site collection lock will return to its original state. The backup package will record the original site collection lock state so that it is restored to that state.  <br/> If users are writing to the site collection while the site collection is being backed up, then the **NoSiteLock** parameter is not recommended for potential impact to backup integrity  <br/> |
| _UseABSDocStreamInfo_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to save the Windows Azure BLOB location information in backup file instead of have the full content in backup file.  <br/> |
| _UseSqlSnapshot_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies a SQL Database Snapshot will be created when the backup begins, and all site collection data will be retrieved directly from the database snapshot. This snapshot will be deleted automatically when the backup completes  <br/> The **UseSqlSnapshot** parameter is recommended if the database server hosting your content database supports database snapshots such as SQL Server Enterprise Edition and SQL Server Developer Edition. This is because it will ensure a valid backup while allowing users to continue reading and writing to the site collection during the backup. It is not necessary to specify the **NoSiteLock** parameter when specifying the **UseSqlSnapshot** parameter.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Get-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/get-spsite.md)
  
[Move-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/move-spsite.md)
  
[Restore-SPSite](restore-spsite.md)
  
[Set-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/set-spsite.md)
  
[Get-SPSiteAdministration](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/get-spsiteadministration.md)

