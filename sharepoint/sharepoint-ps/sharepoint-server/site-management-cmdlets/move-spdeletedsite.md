---
title: "Move-SPDeletedSite"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9a6ba8aa-f9c9-4b05-a9a2-1bb091c11451

description: "Moves deleted site collections from one content database to another."
---

# Move-SPDeletedSite

Moves deleted site collections from one content database to another.
  
```
Move-SPDeletedSite [-Identity] <SPDeletedSitePipeBind> -DestinationDatabase <SPContentDatabasePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-ContentDatabase <SPContentDatabasePipeBind>] [-RbsProviderMapping <Hashtable>] [-WebApplication <SPWebApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Move-SPDeletedSite** cmdlet to move data in a specified site collection from its current content database to the content database specified by the **DestinationDatabase** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPDeletedSitePipeBind  <br/> |Specifies the identity of the site collection to be moved. For example, http://servername/sites/sitename.  <br/> |
|**DestinationDatabase** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the content database that the site collection should be moved to. For example, ContentDB2.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**ContentDatabase** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the SQL Server content database where the site collection data will be stored. If no content database is specified, the content database with the greatest unused site collection capacity and whose database status is ready will be used.  <br/> |
|**RbsProviderMapping** <br/> |Optional  <br/> |System.Collections.Hashtable  <br/> |Used to move a Remote BLOB Storage (RBS)-enabled site collection from one RBS-enabled content database to another RBS-enabled content database without moving the underlying Binary Large Object (BLOB) content. If the content database has more than one RBS provider associated with it, you must specify all providers. The same providers must be enabled on the target content database and the source content database.  <br/> |
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the URL, GUID, or name of the Web application from which to list sites.  <br/> The type must be a valid URL in the form http://server_name; a valid GUID, for example, 12345678-90ab-cdef-1234-567890bcdefgh; or the Web application name, for example, WebApplication1212.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPDeletedSitePipeBind  <br/> ||
|**DestinationDatabase** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ContentDatabase** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> ||
|**RbsProviderMapping** <br/> |Optional  <br/> |System.Collections.Hashtable  <br/> ||
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

----------EXAMPLE---------- 
  
```
Move-SPDeletedSite -Identity 610857cb-8414-4a89-8bf3-ad3628f6c86c -DestinationDatabase "ContentDB2"
```

This example moves deleted site collections from the specified GUID to the database named "ContentDB2".
  
## See also

#### 

[Get-SPDeletedSite](get-spdeletedsite.md)
  
[Remove-SPDeletedSite](remove-spdeletedsite.md)
  
[Restore-SPDeletedSite](restore-spdeletedsite.md)

