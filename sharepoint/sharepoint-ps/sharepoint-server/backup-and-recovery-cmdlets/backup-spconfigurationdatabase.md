---
title: "Backup-SPConfigurationDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 28ddc176-1b7f-47dd-868f-39b7c403a900

description: "Performs a farm-level configuration-only backup."
---

# Backup-SPConfigurationDatabase

Performs a farm-level configuration-only backup.
  
```
Backup-SPConfigurationDatabase -Directory <String> [-AssignmentCollection <SPAssignmentCollection>] [-DatabaseCredentials <PSCredential>] [-DatabaseName <String>] [-DatabaseServer <String>] [-Item <String>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Backup-SPConfigurationDatabase** cmdlet performs a configuration-only backup of the current farm or a configuration-only backup of a separate configuration database which is not attached to the current farm. If you wish to perform a configuration-only backup of the current farm, there is no need to specify the **DatabaseServer** and **DatabaseName** parameters. 
  
An example of a configuration backup is an administrator creates a farm configuration template which then can be applied to other SharePoint farms by performing a restore using the **Restore-SPFarm** cmdlet. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Directory** <br/> |Required  <br/> |System.String  <br/> |Specifies the path where SharePoint stores the backup package it generates. If you have a computer on which SQL Server 2008 and an instance of SharePoint 2013 are installed, you can use local drive paths. This includes a basic installation. However, if SQL Server 2008 and SharePoint 2013 Products are installed on multiple computers or if you have multiple servers running SharePoint 2013 , you must use Universal Naming Convention (UNC) share paths so that the SQL Server database and search components are written to the same location; for example, \\computer_name\volume\Backup).  <br/> Multiple backup packages can be stored in the same location. This is the same path that you pass to the **Directory** parameter of the **Restore-SPFarm** cmdlet.  <br/> The type must be either of the valid paths:  <br/> - C:\ _folder_name_ <br/> -  _\\server_name\folder_name_ <br/> > [!NOTE]> The spbr\* folders are automatically created.           |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the ID and password that corresponds to the administrator user name for the SQL Server database.  <br/> This parameter should only be specified if SQL authentication is used to connect to the database. If Windows authentication is used to connect to the database, then this parameter should not be specified.  <br/> |
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the configuration database name.  <br/> |
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> |Specifies the SQL database server that contains the configuration database. The default value is the local computer name.  <br/> The type must be a valid database server; for example, DS.  <br/> |
|**Item** <br/> |Optional  <br/> |System.String  <br/> |Indicates the part of the farm to back up. You may use the full farm path notation as displayed by the **ShowTree** parameter or the name of the target component in the path if the component has a unique name. If multiple items match the name, the full path must be provided. Surround the item or path in quotation marks if it contains a space.  <br/> If the **Item** parameter is not specified, the entire farm configuration is backed up.  <br/> |
|**ShowTree** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays which objects in the farm will be backed up based on the other parameters passed to the backup cmdlet, namely the **Item** parameter. Items that will be excluded from the backup based on the other parameters passed to the **Backup-SPConfigurationDatabase** cmdlet will be preceded with an asterisk character (*). Items that cannot be backed up will be enclosed in square brackets ([ ]). A backup will not be performed if the **ShowTree** parameter is present.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Directory** <br/> |Required  <br/> |System.String  <br/> ||
|**ShowTree** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**Item** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

-------------------EXAMPLE 1--------------------
  
```
Backup-SPConfigurationDatabase -DatabaseName SharePoint_Config -DatabaseServer SqlServer1 -Directory \\server\share\Backup -ShowTree
```

This example displays components that are available for inclusion in a configuration-only backup.
  
-------------------EXAMPLE 2--------------------
  
```
Backup-SPConfigurationDatabase -DatabaseName SharePoint_Config -DatabaseServer SqlServer1 -Directory \\server\share\Backup -Verbose
```

This example performs a configuration-only backup with verbose output.
  
## See also

#### 

[Connect-SPConfigurationDatabase](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/database-cmdlets/connect-spconfigurationdatabase.md)
  
[Disconnect-SPConfigurationDatabase](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/database-cmdlets/disconnect-spconfigurationdatabase.md)
  
[New-SPConfigurationDatabase](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/database-cmdlets/new-spconfigurationdatabase.md)
  
[Remove-SPConfigurationDatabase](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/database-cmdlets/remove-spconfigurationdatabase.md)
  
[Restore-SPFarm](restore-spfarm.md)

