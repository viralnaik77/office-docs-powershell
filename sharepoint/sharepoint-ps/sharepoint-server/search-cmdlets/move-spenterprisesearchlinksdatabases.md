---
title: "Move-SPEnterpriseSearchLinksDatabases"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 2/18/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5bff925f-3845-434e-be9f-3ba50673be28

description: "Repartitions data and moves it across links databases."
---

# Move-SPEnterpriseSearchLinksDatabases

Repartitions data and moves it across links databases.
  
```
Move-SPEnterpriseSearchLinksDatabases -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-RepartitioningId <Guid>] [-SourceStores <LinksStore[]>] [-TargetStores <LinksStore[]>] [-WhatIf [<SwitchParameter>]]

```

## Example

-------EXAMPLE 1-------
  
```
$ssa=Get-SPEnterpriseSearchServiceapplication
$ssa | New-SPEnterpriseSearchLinksDatabase -DatabaseName "links1"
$ssa | New-SPEnterpriseSearchLinksDatabase -DatabaseName "links2"
$ssa | New-SPEnterpriseSearchLinksDatabase -DatabaseName "links3"
$dbs = $ssa | Get-SPEnterpriseSearchLinksDatabase
$ssa | Move-SPEnterpriseSearchLinksDatabases -TargetStores $dbs
```

This example adds three new links databases and repartitions the data across the existing and new links databases. First, we create the three new links databases. Then we define $dbs, which references the existing and new links databases. Finally, we use **Move-SPEnterpriseSearchLinksDatabases** to repartition the data across the existing and new links databases. 
  
-------EXAMPLE 2-------
  
```
$ssa=Get-SPEnterpriseSearchServiceapplication
$ssa | New-SPEnterpriseSearchLinksDatabase -DatabaseName "links2"
$targetdb = $ssa | Get-SPEnterpriseS-earchLinksDatabase -Identity links2
$sourcedb = $ssa | Get-SPEnterpriseSearchLinksDatabase "links1"
$ssa | Move-SPEnterpriseSearchLinksDatabases -SourceStores $sourcedb -TargetStores $targetdb
```

This example adds one new links database and moves data from the existing links database to the new links database. First, we create a links database named "links2". Then we define $targetdb, which references the new links database "links2". We assume that the Search service application referenced by $ssa has a links store database named "links1". We define $sourcedb, which references the old links database "links1". Finally, we use **Move-SPEnterpriseSearchLinksDatabases** to move the data from "links1" to "links2". When the move is complete, you can remove "links1". 
  
## Detailed Description

A links database stores query logging and analytics information. The **Move-SPEnterpriseSearchLinksDatabases** cmdlet moves this data across a given list of links databases during farm configuration and scale out, to improve the performance and resource load of the farm. Once the move has started, the cmdlet will return a unique identifier, the **RepartitioningId**. Use this identifier to retrigger if the current run fails. After the move has finished, the old databases can be removed. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the links database. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _RepartitioningId_ <br/> |Optional  <br/> |System.Guid  <br/> |Resumes the move with this identifier.  <br/> |
| _SourceStores_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.LinksStore[]  <br/> |Specifies a source list of databases. If this parameter is not specified then all currently existing links databases will be used as a source list.  <br/> |
| _TargetStores_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.LinksStore[]  <br/> |Specifies a target list of databases. If this parameter is not specified then all currently existing links databases will be used as a target list.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**RepartitioningId** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**SourceStores** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.LinksStore[]  <br/> ||
|**TargetStores** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.LinksStore[]  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchLinksDatabase](new-spenterprisesearchlinksdatabase.md)
  
[Set-SPEnterpriseSearchLinksDatabase](set-spenterprisesearchlinksdatabase.md)
  
[Get-SPEnterpriseSearchLinksDatabase](get-spenterprisesearchlinksdatabase.md)
  
[Remove-SPEnterpriseSearchLinksDatabase](remove-spenterprisesearchlinksdatabase.md)

