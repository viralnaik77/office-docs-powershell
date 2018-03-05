---
title: "Get-SPEnterpriseSearchLinksDatabase"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67cf6817-d2d7-4657-b532-fd123ca0da61

description: "Retrieves a reference to a links database."
---

# Get-SPEnterpriseSearchLinksDatabase

Retrieves a reference to a links database.
  
```
Get-SPEnterpriseSearchLinksDatabase -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <LinksStorePipeBind>]

```

## Example

---------EXAMPLE---------
  
```
$linksDatabase = Get-SPEnterpriseSearchLinksDatabase  -Identity LinksDB_1 -SearchApplication MySearchServiceApp
```

This example gets a reference to the links database LinksDB_1 from the search service application MySearchServiceApp.
  
## Detailed Description

The **Get-SPEnterpriseSearchLinksDatabase** cmdlet returns a LinksStore object for use during configuration and when a links database for a search service application is modified or deleted. A links database stores query logging and search analytics data for a search service application. If the **Identity** parameter is not specified, this cmdlet returns all links databases for the specified search application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the links database. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.LinksStorePipeBind  <br/> |Specifies the links database to get. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a LinksStore object, in the form LinksStore1; or an instance of a valid LinksStore object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.LinksStorePipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchLinksDatabase](new-spenterprisesearchlinksdatabase.md)
  
[Set-SPEnterpriseSearchLinksDatabase](set-spenterprisesearchlinksdatabase.md)
  
[Remove-SPEnterpriseSearchLinksDatabase](remove-spenterprisesearchlinksdatabase.md)
#### 

[Move-SPEnterpriseSearchLinksDatabases](move-spenterprisesearchlinksdatabases.md)

