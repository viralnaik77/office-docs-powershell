---
title: "New-SPConfigurationDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 9/9/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b04f1577-1985-41b8-b555-2f5145a00241

description: "Creates a new configuration database."
---

# New-SPConfigurationDatabase

Creates a new configuration database.
  
```
New-SPConfigurationDatabase -DatabaseName <String> -DatabaseServer <String> -FarmCredentials <PSCredential> -Passphrase <SecureString> [-AdministrationContentDatabaseName <String>] [-AssignmentCollection <SPAssignmentCollection>] [-DatabaseCredentials <PSCredential>] [-DatabaseFailOverServer <String>] [-DirectoryDomain <String>] [-DirectoryOrganizationUnit <String>] [-LocalServerRole <Invalid | WebFrontEnd | Application | SingleServer | SingleServerFarm | DistributedCache | Search | Custom | ApplicationWithSearch | WebFrontEndWithDistributedCache>] [-ServerRoleOptional <SwitchParameter>] [-SkipRegisterAsDistributedCacheHost <SwitchParameter>]

```

## Example

------------------EXAMPLE 1-----------------------
  
```
New-SPConfigurationDatabase -DatabaseName "SharePointConfigDB1" -DatabaseServer "SQL-01" -Passphrase (ConvertTo-SecureString "MyPassword" -AsPlainText -force) -FarmCredentials (Get-Credential)
```

This example prompts the user to provide user credentials for the default Farm Administrator account.
  
------------------EXAMPLE 2-----------------------
  
```
New-SPConfigurationDatabase -DatabaseName "SharePointConfigDB1" -DatabaseServer "SQL-01" -Passphrase (ConvertTo-SecureString "MyPassword" -AsPlainText -force) -FarmCredentials (Get-Credential) -LocalServerRole SingleServerFarm
```

This example creates a new configuration database that uses the SingleServerFarm server role type.
  
## Detailed Description

The **New-SPConfigurationDatabase** cmdlet creates a new configuration database on the specified database server. This is the central database for a new SharePoint farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _DatabaseName_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the new configuration database.  <br/> |
| _DatabaseServer_ <br/> |Required  <br/> |System.String  <br/> |Specifies the database server on which to create the configuration database. If no value is specified, the default value is used.  <br/> |
| _FarmCredentials_ <br/> |Required  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies credentials for the Farm Administrator account.  <br/> |
| _Passphrase_ <br/> |Required  <br/> |System.Security.SecureString  <br/> |Specifies the secure password phrase for the new farm. This passphrase is used to join other machines to this farm.  <br/> |
| _AdministrationContentDatabaseName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name for the Central Administration content database for the new farm. If no name is specified, a default name is used.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _DatabaseCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the **Credential** object for the database user. Use this parameter if you use SQL Server Authentication. If no database credentials are provided, Windows authentication is used.  <br/> |
| _DatabaseFailOverServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the mirror server for failover.  <br/> |
| _DirectoryDomain_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the directory domain for the new farm. If no domain is specified, the domain in which the local computer is located is used.  <br/> |
| _DirectoryOrganizationUnit_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the directory organizational unit for the new configuration database. If no organizational unit is specified, the organizational unit in which the local computer is located is used.  <br/> |
| _LocalServerRole_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPServerRole  <br/> |Specifies which Server Role type to use. The valid values are the following:  <br/> - **WebFrontEnd** <br/> - **Application** <br/> - **DistributedCache** <br/> - **Search** <br/> - **SingleServerFarm** <br/> - **Custom** <br/> - **ApplicationWithSearch** <br/> - **WebFrontEndWithDistributedCache** <br/> |
| _ServerRoleOptional_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Configures the farm to not require a server role to be specified. If no server role is specified, the server defaults to the Custom role.  <br/> |
| _SkipRegisterAsDistributedCacheHost_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |By default all the servers in the farm are registered as a cache host (that is, **DistributedCacheService** is running by default).  <br/> Use this parameter to not register the server computer as a distributed cache host. If you want to have a dedicated cache host, then use this parameter to make sure that caching service is not installed on the computer.  <br/> |
| _SiteMapDatabaseName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the database name of the Site Map site.  <br/> |
| _SiteMapDatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the database server name of the Site Map site.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**DatabaseName** <br/> |Required  <br/> |System.String  <br/> ||
|**DatabaseServer** <br/> |Required  <br/> |System.String  <br/> ||
|**DirectoryDomain** <br/> |Optional  <br/> |System.String  <br/> ||
|**DirectoryOrganizationUnit** <br/> |Optional  <br/> |System.String  <br/> ||
|**AdministrationContentDatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**FarmCredentials** <br/> |Required  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**Passphrase** <br/> |Required  <br/> |System.Security.SecureString  <br/> ||
|**SkipRegisterAsDistributedCacheHost** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[Backup-SPConfigurationDatabase](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/backup-and-recovery-cmdlets/backup-spconfigurationdatabase.md)
  
[Disconnect-SPConfigurationDatabase](disconnect-spconfigurationdatabase.md)
  
[Connect-SPConfigurationDatabase](connect-spconfigurationdatabase.md)
  
[Remove-SPConfigurationDatabase](remove-spconfigurationdatabase.md)
  
[Dismount-SPContentDatabase](dismount-spcontentdatabase.md)

