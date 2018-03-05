---
title: "Get-SPEnterpriseSearchQuerySuggestionCandidates"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 456b9bad-3b38-4688-958c-90a59a43cf3a

description: "Returns a list of queries."
---

# Get-SPEnterpriseSearchQuerySuggestionCandidates

Returns a list of queries.
  
```
Get-SPEnterpriseSearchQuerySuggestionCandidates -Owner <SearchObjectOwner> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-SourceId <Guid>]

```

## Example

---------------------EXAMPLE------------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication
```

```
Get-SPEnterpriseSearchQuerySuggestionCandidates -SearchApplication $searchapp
```

This example returns popular search queries by using the search application contained in the variable  `$searchapp`.
  
## Detailed Description

Use the **Get-SPEnterpriseSearchQuerySuggestionCandidates** cmdlet to return a list of popular queries that can be displayed in a related queries Web Part. The list gives the administrator a chance to review potential queries and add some of them to the related queries list. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Owner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the search object owner that defines the scope at which the corresponding **LanguageResourcePhrase** is created.  <br/> The owner must be one of the following valid levels:  <br/> - Search Service Application  <br/> - Site Subscription  <br/> - Site Collection  <br/> - Site  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the query topology.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _SourceId_ <br/> |Optional  <br/> |System.Guid  <br/> |Identifies the search result source for which the **LanguageResourcePhrase** applies to.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Owner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**SourceId** <br/> |Optional  <br/> |System.Guid  <br/> ||
   

