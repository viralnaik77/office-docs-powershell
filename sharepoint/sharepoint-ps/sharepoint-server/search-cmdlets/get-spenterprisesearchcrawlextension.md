---
title: "Get-SPEnterpriseSearchCrawlExtension"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab5860a7-1570-4451-863a-f231191eeb5b

description: "Returns the file types to be included in the content index."
---

# Get-SPEnterpriseSearchCrawlExtension

Returns the file types to be included in the content index.
  
```
Get-SPEnterpriseSearchCrawlExtension -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <ExtensionPipeBind>]

```

## Example

Add code example. 
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication "Sample Search Service Application"$searchapp | Get-SPEnterpriseSearchCrawlExtension "pdf"
```

This example checks whether the  `pdf` file type is included in the file types to be included in the content index. 
  
## Detailed Description

The **Get-SPEnterpriseSearchCrawlExtension** cmdlet returns any or all file extensions in the index for a search application. 
  
Run this cmdlet at the initial search configuration, and after any new IFilter interface is added to read the rule when you create, update, or delete the extension rule. If the **Identity** parameter is not specified, this cmdlet returns the crawl extension collection for the specified search application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the extension collection.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ExtensionPipeBind  <br/> |Specifies the file name extension to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid file name extension (for example, .xml); or an instance of a valid **CrawlExtension** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ExtensionPipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchCrawlExtension](new-spenterprisesearchcrawlextension.md)
  
[Remove-SPEnterpriseSearchCrawlExtension](remove-spenterprisesearchcrawlextension.md)

