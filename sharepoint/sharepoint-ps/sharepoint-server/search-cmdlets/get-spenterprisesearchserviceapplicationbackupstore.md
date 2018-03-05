---
title: "Get-SPEnterpriseSearchServiceApplicationBackupStore"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b306c983-ce99-4a8d-b840-5db542ba4ed0

description: "Retrieves information about the Search service application backup files."
---

# Get-SPEnterpriseSearchServiceApplicationBackupStore

Retrieves information about the Search service application backup files.
  
```
Get-SPEnterpriseSearchServiceApplicationBackupStore -BackupFolder <String> -Name <String> [-AssignmentCollection <SPAssignmentCollection>] [-BackupId <String>] [-Confirm [<SwitchParameter>]] [-IsVerbose <SwitchParameter>] [-UseMostRecent <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE 1-----------------
  
```
Get-SPEnterpriseSearchServiceApplicationBackupStore -BackupFolder \\sample\backup -Name "Search Service Application" -BackupId 3222ad97-91ad-471f-a764-780ec1f05f74
```

This example retrieves the backup of the search databases and index files that are located at  `\\sample\backup` with the backup id  `3222ad97-91ad-471f-a764-780ec1f05f74` from the Search service application  `Search Service Application`. 
  
------------------EXAMPLE 2-----------------
  
```
Get-SPEnterpriseSearchServiceApplicationBackupStore -BackupFolder \\sample\backup -Name "Search Service Application" -UseMostRecent
```

This example retrieves the most recently taken backup of the search databases and index files that are located at  `\\sample\backup` from the Search service application  `Search Service Application`. 
  
## Detailed Description

This cmdlet returns information about the search databases and index files in a specified Search service application backup location.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _BackupFolder_ <br/> |Required  <br/> |System.String  <br/> |Specifies the full file path of the backup files.  <br/> |
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the Search service application from which to retrieve the related backup information.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _BackupId_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the GUID of the backup in the referred package.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _IsVerbose_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |A switch to specify if messages should be printed out when the cmdlet is running.  <br/> |
| _UseMostRecent_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |A switch to specify if the most recent backup should be used.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**BackupFolder** <br/> |Required  <br/> |System.String  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**BackupId** <br/> |Optional  <br/> |System.String  <br/> ||
|**UseMostRecent** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**IsVerbose** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   

