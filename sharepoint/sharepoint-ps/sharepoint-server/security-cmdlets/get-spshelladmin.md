---
title: "Get-SPShellAdmin"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 7/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7081611-c5e2-4ab5-a183-bb5ca8ea8b3d

description: "Returns the names of all users who have the SharePoint_Shell_Access role."
---

# Get-SPShellAdmin

Returns the names of all users who have the **SharePoint_Shell_Access** role. 
  
```
Get-SPShellAdmin [[-database] <SPDatabasePipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Get-SPShellAdmin** cmdlet to return the names of all users who have the **SharePoint_Shell_Access** role in a database. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**database** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPDatabasePipeBind  <br/> |Specifies the GUID of the database or the Databse Object that includes includes the **SharePoint_Shell_Access** role whose user names you want to display. If the **database** parameter is not specified, the configuration database is used.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**database** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPDatabasePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------------EXAMPLE---------------------- 
  
```
Get-SPShellAdmin -database 4251d855-3c15-4501-8dd1-98f960359fa6
```

This example returns the name of each user who has the **SharePoint_Shell_Access** role in the database specified. 
  
## See also

#### 

[Add-SPShellAdmin](add-spshelladmin.md)
  
[Remove-SPShellAdmin](remove-spshelladmin.md)

