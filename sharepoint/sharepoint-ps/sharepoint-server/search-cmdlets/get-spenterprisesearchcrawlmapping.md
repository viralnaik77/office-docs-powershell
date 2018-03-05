---
title: "Get-SPEnterpriseSearchCrawlMapping"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89a24664-f67a-4fe8-bb7c-95bf297c7776

description: "Returns a crawl mapping for the search application."
---

# Get-SPEnterpriseSearchCrawlMapping

Returns a crawl mapping for the search application.
  
```
Get-SPEnterpriseSearchCrawlMapping -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <CrawlMappingPipeBind>]

```

## Example

```
$searchapp = Get-SPEnterpriseSearchServiceApplication "SearchApp1"$searchapp | Get-SPEnterpriseSearchCrawlMapping
```

This example returns the crawl mappings for the search application  `SearchApp1`.
  
## Detailed Description

The **Get-SPEnterpriseSearchCrawlMapping** cmdlet reads a **CrawlMapping** object when one of the crawl mapping rules is created, updated, or deleted. Run this cmdlet when the search is initially configured, and when access is changed through a different mechanism to create the crawl mapping rule; for example, when a rule is changed to use file:\\ rather than http://. 
  
If the **Identity** parameter is not specified, this cmdlet returns the crawl mapping collection for the specified search application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the crawl mapping collection.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawlMappingPipeBind  <br/> |Specifies the crawl mapping to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL, in the form http://crawlmap1; or an instance of a valid **CrawlMapping** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawlMappingPipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchCrawlMapping](new-spenterprisesearchcrawlmapping.md)
  
[Remove-SPEnterpriseSearchCrawlMapping](remove-spenterprisesearchcrawlmapping.md)

