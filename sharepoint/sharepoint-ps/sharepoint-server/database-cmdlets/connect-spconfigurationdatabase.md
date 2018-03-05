---
title: "Connect-SPConfigurationDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 9/9/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44ace210-aab1-4b4f-b133-0a302d89541b

description: "Connects the local server computer to a farm."
---

# Connect-SPConfigurationDatabase

Connects the local server computer to a farm.
  
```
Connect-SPConfigurationDatabase -DatabaseName <String> -DatabaseServer <String> -Passphrase <SecureString> [-AssignmentCollection <SPAssignmentCollection>] [-DatabaseCredentials <PSCredential>] [-DatabaseFailOverPartner <String>] [-LocalServerRole <Invalid | WebFrontEnd | Application | SingleServer | SingleServerFarm | DistributedCache | Search | Custom | ApplicationWithSearch | WebFrontEndWithDistributedCache>] [-SkipRegisterAsDistributedCacheHost <SwitchParameter>]

```

## Example

------------------EXAMPLE 1------------------
  
```
Connect-SPConfigurationDatabase -DatabaseServer "ServerName\InstanceName" -DatabaseName "SharePointConfigurationDatabaseName" -Passphrase (ConvertTo-SecureString "MyP@ssw0rd") -AsPlainText -Force                      
```

```
Start-Service SPTimerv4
```

This example joins the local server computer to a farm that is configured to use the database  `SharePointConfigurationDatabase` on an instance of SQL Server by using the name  `ServerName\InstanceName` with the passphrase  `MyP@ssw0rd`.
  
------------------EXAMPLE 2------------------
  
```
Connect-SPConfigurationDatabase -DatabaseServer "ServerName\InstanceName" -DatabaseName "SharePointConfigurationDatabaseName" -Passphrase (ConvertTo-SecureString "MyP@ssw0rd") -AsPlainText -Force -LocalServerRole SingleServerFarm
```

This example joins the local server computer to a farm that is configured to use the database  `SharePointConfigurationDatabase` with the SingleServerFarm server role type. 
  
## Detailed Description

The **Connect-SPConfigurationDatabase** cmdlet connects the current server to the specified configuration database. 
  
Essentially, this cmdlet connects the server to the farm. If the current computer cannot be connected to a farm, the following error message is displayed: 
  
"This machine is already connected to a SharePoint farm. See: Dismount-SPConfigurationDatabase"
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _DatabaseName_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the configuration database to which to connect the server.  <br/> The type must be a valid database name; for example, DB1.  <br/> |
| _DatabaseServer_ <br/> |Required  <br/> |System.String  <br/> |Specifies the server on which to create the configuration database. The default value is the local computer name.  <br/> |
| _Passphrase_ <br/> |Required  <br/> |System.Security.SecureString  <br/> |Specifies the secure password phrase for connecting the current server to the configuration database.  <br/> The type must be a valid secure string; for example, MyBDCApp1serverkey.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _DatabaseCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the **PSCredential** object that contains the user name and password to be used for database SQL authentication. If this parameter is not specified, the current user is used.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _DatabaseFailOverPartner_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the mirror server for failover.  <br/> |
| _LocalServerRole_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPServerRole  <br/> |Specifies which Server Role type to use. The valid values are the following:  <br/> - **WebFrontEnd** <br/> - **Application** <br/> - **DistributedCache** <br/> - **Search** <br/> - **SingleServerFarm** <br/> - **Custom** <br/> - **ApplicationWithSearch** <br/> - **WebFrontEndWithDistributedCache** <br/> |
| _SkipRegisterAsDistributedCacheHost_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |By default all the servers in the farm are registered as a cache host (that is, **DistributedCacheService** is running by default).  <br/> Use this parameter to not register the server computer as a distributed cache host. If you want to have a dedicated cache host, then use this parameter to make sure that caching service is not installed on the computer.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**DatabaseName** <br/> |Required  <br/> |System.String  <br/> ||
|**Passphrase** <br/> |Required  <br/> |System.Security.SecureString  <br/> ||
|**SkipRegisterAsDistributedCacheHost** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseServer** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
   
## See also

#### 

[Backup-SPConfigurationDatabase](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/backup-and-recovery-cmdlets/backup-spconfigurationdatabase.md)
  
[Disconnect-SPConfigurationDatabase](disconnect-spconfigurationdatabase.md)
  
[Dismount-SPContentDatabase](dismount-spcontentdatabase.md)
  
[New-SPConfigurationDatabase](new-spconfigurationdatabase.md)
  
[Remove-SPConfigurationDatabase](remove-spconfigurationdatabase.md)

