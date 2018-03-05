---
title: "Copy-SPSideBySideFiles"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 11/13/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1a8957db-2c2c-4c64-b54d-0c61d4bf8925

description: "Copy side by side files."
---

# Copy-SPSideBySideFiles

Copy side by side files.
  
```
Copy-SPSideBySideFiles [-AssignmentCollection <SPAssignmentCollection>] [-LogFile <String>]

```

## Example

--------------EXAMPLE 1-----------------
  
```
Copy-SPSideBySideFiles -LogFile "C:\CopySideBySideFiles.log"
```

This example copies SideBySide files and writes a log data of the copy process to the CopySideBySideFiles.log file.
  
## Detailed Description

In SharePoint Server 2016, zero down time in-place upgrade is available. If the PSConfig.exe file is used during an upgrade and copy SideBySide files fail, you can use the **Copy-SPSideBySideFiles** cmdlet to copy SideBySide files. If you use Microsoft PowerShell scripts instead of PSConfig.exe to perform an upgrade, please run the **Copy-SPSideBySideFiles** cmdlet to copy SideBySide files. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _LogFile_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the fully-qualified logfile name of SideBySide copy operation. If LogFile is not specified, the logfile will be placed in default SharePoint log files folder.  <br/> |
   

