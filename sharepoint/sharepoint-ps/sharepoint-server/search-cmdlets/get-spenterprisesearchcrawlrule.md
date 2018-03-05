---
title: "Get-SPEnterpriseSearchCrawlRule"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a99f98a2-82b2-4336-a14f-1bc527129e8d

description: "Accesses crawl rules."
---

# Get-SPEnterpriseSearchCrawlRule

Accesses crawl rules.
  
```
Get-SPEnterpriseSearchCrawlRule -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <CrawlRulePipeBind>]

```

## Example

---------------EXAMPLE 1----------------- 
  
```
$searchApp = Get-SPEnterpriseSearchServiceApplication ExampleSearchServiceApplication $crawlRule = Get-SPEnterpriseSearchCrawlRule -SearchApplication  $searchApp -Identity http://example$crawlRule | Set-SPEnterpriseSearchCrawlRule -Type InclusionRule
```

This example uses the **Get-SPEnterpriseSearchCrawlRule** cmdlet to retrieve a crawl rule in order to change its type from  `ExclusionRule` to  `InclusionRule`.
  
---------------EXAMPLE 2---------------
  
```
$searchApp = Get-SPEnterpriseSearchServiceApplication MySearchServiceApp Get-SPEnterpriseSearchCrawlRule -SearchApplication $searchApp | where {$_.Path -like "*example*"}
```

This example returns a list of crawl rules with paths that contain the word  `example` from the search service application named,  `MySearchServiceApp`.
  
## Detailed Description

Use the **Get-SPEnterpriseSearchCrawlRule** cmdlet for a search administrator to run this procedure to retrieve the crawl rule when the crawl rule is updated or deleted. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the crawl rule. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawlRulePipeBind  <br/> |Specifies the search crawl rule path. A valid URL, such as "http://server_name", or an instance of a valid **CrawlRule** object  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawlRulePipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchCrawlRule](new-spenterprisesearchcrawlrule.md)
  
[Set-SPEnterpriseSearchCrawlRule](set-spenterprisesearchcrawlrule.md)
  
[Remove-SPEnterpriseSearchCrawlRule](remove-spenterprisesearchcrawlrule.md)

