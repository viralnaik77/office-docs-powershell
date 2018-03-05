---
title: "Remove-SPShellAdmin"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 7/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dcccc7b2-4c82-4966-b5cb-76f18bd4eb99

description: "Removes a user from the SharePoint_Shell_Access role."
---

# Remove-SPShellAdmin

Removes a user from the **SharePoint_Shell_Access** role. 
  
```
Remove-SPShellAdmin [-UserName] <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-database <SPDatabasePipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Remove-SPShellAdmin** cmdlet to remove a user from the **SharePoint_Shell_Access** role in a specified database. 
  
When you use this cmdlet to remove a user from the role, you do not remove the user from the **WSS_ADMIN_WPG** group in the target database. 
  
When you run this cmdlet to add a user to the **SharePoint_Shell_Access** role, the user must have the following security permissions: 
  
- **Security_Admin** role access on the instance of SQL Server and the **db_owner** role in the database. 
  
- Administrative permission to the local computer.
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**UserName** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the user you want to remove from the **SharePoint_Shell_Access** role in the specified database.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**database** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPDatabasePipeBind  <br/> |Specifies the GUID of the database or the Databse Object that includes the **SharePoint_Shell_Access** role from which the user is to be removed. If the **database** parameter is not specified, the configuration database is used.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**UserName** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**database** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPDatabasePipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------------------EXAMPLE-----------------------------
  
```
Remove-SPShellAdmin -UserName CONTOSO\User1 -database 4251d855-3c15-4501-8dd1-98f960359fa6
```

This example removes an existing user named  `User1` from the **SharePoint_Shell_Access** role in the database specified. 
  
## See also

#### 

[Add-SPShellAdmin](add-spshelladmin.md)
  
[Get-SPShellAdmin](get-spshelladmin.md)

