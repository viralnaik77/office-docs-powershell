---
title: "Restore-SPSite"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 90f19a58-0455-470c-a8ee-3129fc341f62

description: "Restores a site collection."
---

# Restore-SPSite

Restores a site collection.
  
```
Restore-SPSite [-Identity] <String> -Path <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-ContentDatabase <SPContentDatabasePipeBind>] [-Force <SwitchParameter>] [-GradualDelete <SwitchParameter>] [-HostHeaderWebApplication <String>] [-PreserveSiteID <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
 The **Restore-SPSite** cmdlet performs a restoration of the site collection to a location specified by the **Identity** parameter. A content database may only contain one copy of a site collection. If a site collection is backed up and restored to a different URL location within the same Web application, an additional content database must be available to hold the restored copy of the site collection. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |System.String  <br/> | Specifies the URL location to which the site collection is restored.  <br/>  A site collection does not have to already exist at the URL location to perform a restore. However, you must specify a valid URL location that a site collection can be created. If a site collection already exists at the specified URL location, you must specify the **Force** parameter to overwrite it.  <br/> The type must be a valid URL, in the form http://server_name/sites/site_name.  <br/> |
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies a valid path to the location of the backup. For example, C:\Backup\site_name.bak.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**ContentDatabase** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the SQL Server content database where the site collection data will be stored. If no content database is specified, the content database with the greatest unused site collection capacity and whose database status is ready will be used.  <br/> |
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> | Specifies the SQL Server content database where the site collection data will be stored. If no content database is specified, the content database with the greatest unused site collection capacity and whose database status is ready will be used.  <br/> The type must be a valid database name, in the form SQLDB1.  <br/> |
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> | Specifies the name of the SQL Server containing the content database specified by the **DatabaseName** parameter.  <br/> The type must be a valid database server name, in the form SQLBE1 and needs to be used in conjunction with the **DatabaseName** parameter.  <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> | Specifies that the existing site collection at the URL location is to be overwritten by this restoration.  <br/> |
|**GradualDelete** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> | Specifies that the site collection being overwritten with the **Force** parameter should be gradually deleted over time by a timer job instead of all at once, which reduces its impact on SharePoint 2010 Products and SQL Server performance. This option is recommended for large site collections.  <br/> |
|**HostHeaderWebApplication** <br/> |Optional  <br/> |System.String  <br/> |A valid URL assigned to the Web application by using alternate access mapping, such as http:// _server_name_ <br/> Restores a site collection as a host-named site collection instead of a path-based site collection. When the **HostHeaderWebApplication** parameter is present, the value of the **Identity** parameter is the URL of the host-named site collection and the value of the **HostHeaderWebApplication** parameter is the URL of the Web application that will hold the host-named site collection.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

----------------------EXAMPLE 1---------------------- 
  
```
Restore-SPSite http://server_name/sites/site_name -Path C:\Backup\site_name.bak
```

This example restores a site collection from the backup file  `C:\Backup\site_name.bak` to the site collection URL  `http://server_name/sites/site_name`.
  
----------------------EXAMPLE 2---------------------- 
  
```
Restore-SPSite http://server_name/sites/site_name -Path C:\Backup\site_name.bak -Force -DatabaseServer SQLBE1 -DatabaseName SQLDB1
```

This example restores a site collection backup from the backup file  `C:\Backup\site_name.bak`, but overwrites the existing site collection at  `http://server_name/sites/site_name` while specifying that the site collection must be stored in a specific content database. 
  
----------------------EXAMPLE 3---------------------- 
  
```
Restore-SPSite http://www.example.com -Path \\file_server\share\site_name.bak -HostHeaderWebApplication http://server_name
```

 This example restores a site collection backup from the backup file  `\\file_server\share\site_name.bak` to the host-named site collection  `http://www.example.com` on the Web application  `http://server_name`.
  
## See also

#### 

[Backup-SPSite](backup-spsite.md)
  
[Get-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/get-spsite.md)
  
[Move-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/move-spsite.md)
  
[New-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/new-spsite.md)
  
[Remove-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/remove-spsite.md)
  
[Set-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/set-spsite.md)

