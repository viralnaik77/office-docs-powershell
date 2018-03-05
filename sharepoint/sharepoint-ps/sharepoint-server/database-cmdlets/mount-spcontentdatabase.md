---
title: "Mount-SPContentDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20d1bc07-805c-44d3-a278-e2793370e237

description: "Attaches an existing content database to the farm."
---

# Mount-SPContentDatabase

Attaches an existing content database to the farm.
  
```
Mount-SPContentDatabase -Name <String> -WebApplication <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-AssignNewDatabaseId <SwitchParameter>] [-ChangeSyncKnowledge <SwitchParameter>] [-ClearChangeLog <SwitchParameter>] [-Confirm [<SwitchParameter>]] [-DatabaseAccessCredentials <PSCredential>] [-DatabaseCredentials <PSCredential>] [-DatabaseFailoverServer <String>] [-DatabaseServer <String>] [-MaxSiteCount <Int32>] [-SkipIntegrityChecks <SwitchParameter>] [-SkipSiteUpgrade <SwitchParameter>] [-UseLatestSchema <SwitchParameter>] [-WarningSiteCount <Int32>] [-WhatIf [<SwitchParameter>]]

```

## Example

-----------------EXAMPLE 1---------------------
  
```
Mount-SPContentDatabase "MyDatabase" -DatabaseServer "MyServer" -WebApplication http://sitename
```

This example mounts an existing database to the sitename web application. If upgrades are required, it triggers database schema upgrade and then performs only build-to-build upgrade actions on existing site collections if required. This operation does not changed the CompatibilityLevel for existing site collections in this database.
  
-----------------EXAMPLE 2---------------------
  
```
Mount-SPContentDatabase "MyDatabase" -DatabaseServer "MyServer" -WebApplication http://sitename -NoB2BSiteUpgrade
```

This example mounts an existing database to the sitename web application but it prevents any site upgrades from occurring. If upgrades are required, it triggers database schema upgrades only and no build-to-build upgrade actions are performed on any site collections. This operation does not change the CompatibilityLevel for existing site collections in this database.
  
## Detailed Description

The **Mount-SPContentDatabase** cmdlet attaches an existing content database to the farm. If the database being mounted requires an upgrade, this cmdlet will cause the database to be upgraded. 
  
The default behavior of this cmdlet causes an upgrade of the schema of the database and initiates upgraded builds for all site collections within the specified content database if required. To prevent initiation of upgraded builds of site collections, use the **NoB2BSiteUpgrade** parameter. This cmdlet does not trigger version-to-version upgrade of any site collections. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the existing content database to attach to the farm.  <br/> The type must be a valid name of a SharePoint content database; for example, SPContentDB1.  <br/> |
| _WebApplication_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Attaches the content database to the specified SharePoint web application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of SharePoint web application (for example, MyOfficeApp1); or an instance of a valid **SPWebApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _AssignNewDatabaseId_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Creates a new database ID automatically when the content database is attached.  <br/> |
| _ChangeSyncKnowledge_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Database attach will cause all Groove sync client to re-synchronize their content.  <br/> |
| _ClearChangeLog_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Clears any pending changes from the change log in the content database.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseAccessCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the credential that belong to **SPDataAccess** role.  <br/> |
| _DatabaseCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the **PSCredential** object that contains the user name and password to be used for database SQL Authentication.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _DatabaseFailoverServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the database server to be mirrored.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the content database specified in the **Name** parameter.  <br/> The type must be a valid SQL Server host name; for example, SQLServerHost1.  <br/> |
| _MaxSiteCount_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of web sites that can use the content database.  <br/> The type must be a positive integer.  <br/> |
| _SkipIntegrityChecks_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies the upgrade process not to run the internal integrity checks such as missing templates, and orphan detection as part of the upgrade process.  <br/> |
| _SkipSiteUpgrade_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to not upgrade all site objects when performing upgrade.  <br/> |
| _UseLatestSchema_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to use the latest schema. In an on-premises environment, this parameter has no effect.  <br/> There are two values **$True** and **$False**.  <br/> The default value is **False**.  <br/> |
| _WarningSiteCount_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of sites that can be created before a warning event is generated and the owner of the site collection is notified.  <br/> The type must be a positive integer.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Get-SPContentDatabase](get-spcontentdatabase.md)
  
[Set-SPContentDatabase](set-spcontentdatabase.md)
  
[Upgrade-SPContentDatabase](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/upgrade-cmdlets/upgrade-spcontentdatabase.md)
  
[Dismount-SPContentDatabase](dismount-spcontentdatabase.md)
  
[Get-SPServer](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/get-spserver.md)
#### 

[Remove-SPContentDatabase](http://technet.microsoft.com/library/e8c337b6-37af-4fdd-8469-a32f4d45c040.aspx)

