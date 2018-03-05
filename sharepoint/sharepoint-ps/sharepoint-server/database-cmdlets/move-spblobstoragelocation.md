---
title: "Move-SPBlobStorageLocation"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5b66feac-c365-4dfd-9ccb-a66a4faa617f

description: "Copies a content database to a new location by using Remote BLOB Storage (RBS)."
---

# Move-SPBlobStorageLocation

Copies a content database to a new location by using Remote BLOB Storage (RBS).
  
```
Move-SPBlobStorageLocation [-SourceDatabase] <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DestinationDatabase <String>] [-DestinationDataSourceInstance <String>] [-Dir <String>] [-VerboseMod <$true | $false>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Move-SPBlobStorageLocation** cmdlet to use Remote BLOB Storage (RBS) to copy a content database to an instance of a SQL Server database. The database size limitation for SQL Server is 4 gigabytes (GB). If a content database is greater than 4 GB, the database cannot be copied directly to a SQL Server database instance. The **Move-SPBlobStorageLocation** cmdlet uses the advantage of RBS and copies databases larger than 4 GB. RBS stores the data on the local hard disk and keeps the links to the data in the database, which results in a smaller database. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SourceDatabase** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the Windows Internal Database.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DestinationDatabase** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the migrated database. If the **DestinationDatabase** parameter is not specified, the **SourceDatabase** parameter is used.  <br/> |
|**DestinationDataSourceInstance** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the instance of the destination database. The value in the **SourceDatabase** parameter is migrated to this instance. The name of the instance of the database should be SQL Server 2008 with Service Pack 1 (SP1) and Cumulative Update 2 version or higher. If the **DestinationDataSourceInstance** parameter is not specified, the local host name is used.  <br/> |
|**Dir** <br/> |Optional  <br/> |System.String  <br/> |Used for all disk operations, including storing temporary backups and database (.mdf) files of a migrated database. If the **Dir** parameter is not specified, a default directory of the destination SQL Server instance is used. The free space in this directory should be at least two times the size of the source database.  <br/> |
|**VerboseMod** <br/> |Optional  <br/> |System.Boolean  <br/> |Generates verbose log output to be displayed in the Command Prompt window. If the **VerboseMod** parameter is not specified, no output is displayed.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SourceDatabase** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DestinationDatabase** <br/> |Optional  <br/> |System.String  <br/> ||
|**DestinationDataSourceInstance** <br/> |Optional  <br/> |System.String  <br/> ||
|**Dir** <br/> |Optional  <br/> |System.String  <br/> ||
|**VerboseMod** <br/> |Optional  <br/> |System.Boolean  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-------------------EXAMPLE 1-----------------------
  
```
Move-SPBlobStorageLocation WSS_Content
```

This example copies the content database named  `WSS_Content` from the Windows Internal Database to the same database name in SQL Server 2008 Express by using RBS. 
  
-------------------EXAMPLE 2-----------------------
  
```
Move-SPBlobStorageLocation WSS_Content -DestinationDatabase WSS_V4_Content -BackupDatabase WSSBackupDB -VerboseMod:$true
```

This example copies the content database named  `WSS_Content` from the Windows Internal Database to a database in SQL Server 2008 Express. The name of the new database will be  `WSS_V4_Content`. During the move, the backup file name will be  `WSSBackupDB`. The output of this command displays log information to the Command Prompt window.
  

