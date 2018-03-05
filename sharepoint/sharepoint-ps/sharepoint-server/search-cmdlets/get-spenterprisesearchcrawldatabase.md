---
title: "Get-SPEnterpriseSearchCrawlDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d4944100-fea2-4a6c-9ea3-553cd99c856b

description: "Returns a crawl store."
---

# Get-SPEnterpriseSearchCrawlDatabase

Returns a crawl store.
  
```
Get-SPEnterpriseSearchCrawlDatabase -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <CrawlStorePipeBind>]

```

## Example

-------------------EXAMPLE-------------------
  
```
$crawlDatabase = Get-SPEnterpriseSearchCrawlDatabase -SearchApplicationMySearchServiceApp -Identity CrawlDB_1
```

This example gets a reference to the crawl database  `CrawlDB_1` from the search service application named  `MySearchServiceApp`.
  
## Detailed Description

The **Get-SPEnterpriseSearchCrawlDatabase** cmdlet returns a **CrawlStore** object for use during configuration and when a crawl database for a search service application is modified or deleted. A crawl database stores crawl history data for a search service application. 
  
If the **Identity** parameter is not specified, this cmdlet returns the crawl database collection for the specified search application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the crawl database.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawlStorePipeBind  <br/> |Specifies the crawl database to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a **CrawlStore** object, in the form CrawlStore1; or an instance of a valid **CrawlStore** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawlStorePipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchCrawlDatabase](new-spenterprisesearchcrawldatabase.md)
  
[Set-SPEnterpriseSearchCrawlDatabase](set-spenterprisesearchcrawldatabase.md)
  
[Remove-SPEnterpriseSearchCrawlDatabase](remove-spenterprisesearchcrawldatabase.md)

