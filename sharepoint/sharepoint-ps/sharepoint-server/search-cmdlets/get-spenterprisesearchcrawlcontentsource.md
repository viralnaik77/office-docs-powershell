---
title: "Get-SPEnterpriseSearchCrawlContentSource"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2bd3631d-a24d-443f-bab8-a261dc3fb701

description: "Returns a crawl content source."
---

# Get-SPEnterpriseSearchCrawlContentSource

Returns a crawl content source.
  
```
Get-SPEnterpriseSearchCrawlContentSource -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <ContentSourcePipeBind>]

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication " SearchApp1" $contentsource = Get-SPEnterpriseSearchCrawlContentSource -SearchApplication $searchapp -Identity "Local SharePoint Sites" $contentsource.StartFullCrawl()
```

This example retrieves the default content source for the search service application,  `SearchApp1`, and starts a full crawl on the content source.
  
## Detailed Description

The **Get-SPEnterpriseSearchCrawlContentSource** cmdlet reads the content source when the rules of content source are created, updated, or deleted, or reads a **CrawlContentSource** object when the search functionality is initially configured and after any new content source is added. 
  
If the **Identity** parameter is not specified, this cmdlet returns the content source collection for the specified search application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the content source.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ContentSourcePipeBind  <br/> |Specifies the content source to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a **ContentSource** object (for example, ContentSource1); or an instance of a valid **ContentSource** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ContentSourcePipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchCrawlContentSource](new-spenterprisesearchcrawlcontentsource.md)
  
[Set-SPEnterpriseSearchCrawlContentSource](set-spenterprisesearchcrawlcontentsource.md)
  
[Remove-SPEnterpriseSearchCrawlContentSource](remove-spenterprisesearchcrawlcontentsource.md)

