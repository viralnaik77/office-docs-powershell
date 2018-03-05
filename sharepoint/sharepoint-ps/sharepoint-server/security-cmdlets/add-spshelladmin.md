---
title: "Add-SPShellAdmin"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 7/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2ddfad84-7ca8-409e-878b-d09cb35ed4aa

description: "Adds a user to the SharePoint_Shell_Access role for the specified database."
---

# Add-SPShellAdmin

Adds a user to the **SharePoint_Shell_Access** role for the specified database. 
  
```
Add-SPShellAdmin [-UserName] <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-database <SPDatabasePipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

> [!IMPORTANT]
> When you run this cmdlet to add a user to the **SharePoint_Shell_Access** role, you must have membership in the **securityadmin** fixed server role on the SQL Server instance, membership in the **db_owner** fixed database role on all affected databases, and local administrative permission on the local computer. > This cmdlet is intended only to be used with a database that uses Windows authentication. There is no need to use this cmdlet for databases that use SQL authentication; in fact, doing so may result in an error message. 
  
Use the **Add-SPShellAdmin** cmdlet to add a user to the **SharePoint_Shell_Access** role as follows: 
  
--If you specify only the user, the user is added to the role for the farm configuration database. 
  
--If you use the **database** parameter, the user is added to the role on the farm configuration database, the Central Administration content database, and the specified database. Using the **database** parameter is the preferred method because most of the administrative operations require access to the Central Administration content database. 
  
The user is added to the **WSS_Admin_WPG** group on all Web servers when the user is added to the **SharePoint_Shell_Access** role. If the target database does not have a **SharePoint_Shell_Access** role, the role is automatically created. 
  
> [!IMPORTANT]
> A user must be a member of the **SharePoint_Shell_Access** role on the configuration database and a member of the **WSS_ADMIN_WPG** local group on the computer where SharePoint Server is installed. However, the result of running this cmdlet is that the user specified with the **UserName** parameter will have the **db_owner** role access on the affected databases as described above. Therefore, you should carefully plan which users are given this access. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**UserName** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the user to add to the **SharePoint_Shell_Access** role in the target database.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**database** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPDatabasePipeBind  <br/> |Specifies the GUID of the database or the Database object that includes the **SharePoint_Shell_Access** role to which you want to add the user. If the **database** parameter is not specified, the configuration database is used. The farm configuration database is always included, even if you specify another database.  <br/> |
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

-------------------EXAMPLE 1-------------------------
  
```
Add-SPShellAdmin -UserName CONTOSO\User1
```

This example adds a new user named  `User1` to the **SharePoint_Shell_Access** role in the farm configuration database only, and also ensures the user is added to the **WSS_Admin_WPG** local group on each server in the farm. 
  
-------------------EXAMPLE 2-------------------------
  
```
Add-SPShellAdmin -UserName CONTOSO\User1 -database 4251d855-3c15-4501-8dd1-98f960359fa6
```

This example adds a new user named  `User1` to the **SharePoint_Shell_Access** role in both the specified content database and the configuration database by passing a database GUID to the cmdlet. 
  
-------------------EXAMPLE 3-------------------------
  
```
Get-SPDatabase | Where-Object {$_.WebApplication -like "SPAdministrationWebApplication"} | Add-SPShellAdmin CONTOSO\User1
```

This example adds a new user named  `User1` to the **SharePoint_Shell_Access** role in both the specified Central Administration content database and the configuration database. 
  
-------------------EXAMPLE 4-------------------------
  
```
Get-SPDatabase | ?{$_.Name -eq "WSS_Content"} | Add-SPShellAdmin -Username CONTOSO\User1
```

This example adds a new user named  `User1` to the **SharePoint_Shell_Access** role of both the specified content database and the configuration database by passing the name of the database to the cmdlet. 
  
## See also

#### 

[Get-SPShellAdmin](get-spshelladmin.md)
  
[Remove-SPShellAdmin](remove-spshelladmin.md)

