---
title: "Import-SPAccessServicesDatabase"
ms.author: kirks
author: Techwriter40
ms.date: 10/20/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee3fc17f-2924-435d-87bf-3edf0a55f487

description: "Imports the Access Database from a Bacpac package."
---

# Import-SPAccessServicesDatabase

Imports the Access Database from a Bacpac package.
  
```
Import-SPAccessServicesDatabase -Bacpac <Byte[]> -DatabaseName <String> -ServerReferenceId <Guid> [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

------------EXAMPLE 1----------------
  
```
Import-SPAccessServicesDatabase -Bacpac AccessApp.bacpac -DatabaseName $db -ServerReferenceId $id
```

This example imports a Access Services database using the bacpac file, AccessApp.bacpac.
  
## Detailed Description

A Bacpac file is created by SQL Server during an export operation of a database. It contains all the information needed for moving or importing the database to a new SQL Server. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Bacpac_ <br/> |Required  <br/> |System.Byte[]  <br/> |File created from running a backup of the database.  <br/> |
| _DatabaseName_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the database.  <br/> |
| _ServerReferenceId_ <br/> |Required  <br/> |System.Guid  <br/> |Specifies a unique identifier for the database server. Used for maintaining continuity when restoring an existing content database to a different or new farm.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## See also

#### 

[Export-SPAccessServicesDatabase](export-spaccessservicesdatabase.md)

