---
title: "Move-SPSite"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e3bf1b34-78b9-4643-b0dd-24444e3cffc5

description: "Moves site collections from one content database to another."
---

# Move-SPSite

Moves site collections from one content database to another.
  
```
Move-SPSite [-Identity] <SPSitePipeBind> -DestinationDatabase <SPContentDatabasePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-CopyEvents <$true | $false>] [-RbsProviderMapping <Hashtable>] [-WhatIf [<SwitchParameter>]]

```

## Detailed Description

The **Move-SPSite** cmdlet moves the data in the specified site collection from its current content database to the content database specified by the **DestinationDatabase** parameter. A no-access lock is applied to the site collection to prevent users from altering data within the site collection while the move is taking place. Once the move is complete, the site collection is returned to its original lock state. The destination content database specified must already exist, must be attached to the same SQL Server as the site collection's current content database, and must be attached to the site collection's current Web application. 
  
After you run the **Move-SPSite** cmdlet, run the **IISReset** command to update changes to IIS. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the identity of the site collection to be moved. For example, http://servername/sites/sitename.  <br/> |
|**DestinationDatabase** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the content database that the site collection should be moved to. For example, ContentDB2.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CopyEvents** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies if events need to be copied.  <br/> The valid values are **True** or **False**.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**RbsProviderMapping** <br/> |Optional  <br/> |System.Collections.Hashtable  <br/> |
> [!NOTE]
> This parameter was added in SharePoint Server 2010 with Service Pack 1 (SP1) and SharePoint Foundation 2010 with Service Pack 1 (SP1). 
  
Used to move an RBS-enabled site collection from one RBS-enabled content database to another RBS-enabled content database without moving the underlying BLOB content. If the content database has more than one RBS provider associated with it, you must specify all providers. The same providers must be enabled on the target content database and the source content database.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

---------------------EXAMPLE 1-----------------------
  
```
Move-SPSite http://servername/sites/sitename -DestinationDatabase ContentDb2
```

This example moves the site collection http://servername/sites/sitename to the content database ContentDb2.
  
---------------------EXAMPLE 2-----------------------
  
```
Get-SPSite -ContentDatabase ContentDb1 | Move-SPSite -DestinationDatabase ContentDb2
```

This example moves all site collections in ContentDb1 to ContentDb2.
  
---------------------EXAMPLE 3-----------------------
  
```
Get-SPSiteAdministration | where { $_.OwnerLoginName -eq "DOMAIN\username" } | Move-SPSite -DestinationDatabase ContentDb2
```

This example moves all site collections where  _DOMAIN\username_ is the site collection owner to ContentDb2. The **Get-SPSiteAdministration** cmdlet is used instead of the **Get-SPSite** cmdlet because you must have permission within the site collection to access the properties of the **SPSite** object. You can access the properties of the **SPSiteAdministration** object as a SharePoint farm administrator. 
  
---------------------EXAMPLE 4-----------------------
  
```
Move-SPSite -Identity siteUrl -DestinationDatabase databaseName -RbsProviderMapping       @{"sourceProvider1"="targetProvider1", "sourceProvider2"="targetProvider2"}
```

This example moves an RBS-enabled site collection from one RBS-enabled content database to another RBS-enabled content database, **sourceProvider1** is the source RBS provider and **targetProvider1** is the target RBS provider. 
  
## See also

#### 

[Backup-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/backup-and-recovery-cmdlets/backup-spsite.md)
  
[Get-SPSite](get-spsite.md)
  
[Restore-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/backup-and-recovery-cmdlets/restore-spsite.md)
  
[Get-SPSiteAdministration](get-spsiteadministration.md)

