---
title: "Get-SPEnterpriseSearchSiteHitRule"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ba0d415d-5b7e-4392-9a80-c73292b2294e

description: "Returns the shared site hit rule."
---

# Get-SPEnterpriseSearchSiteHitRule

Returns the shared site hit rule.
  
```
Get-SPEnterpriseSearchSiteHitRule [-AssignmentCollection <SPAssignmentCollection>] [-Identity <SiteHitRulePipeBind>] [-SearchService <SearchServicePipeBind>]

```

## Example

------------------EXAMPLE------------------
  
```
$shRule = Get-SPEnterpriseSearchSiteHitRule -Identity MySiteHitRule
```

The following example obtains a reference to the site hit rule with the name  `MySiteHitRule`.
  
## Detailed Description

The **Get-SPEnterpriseSearchSiteHitRule** cmdlet reads a **SiteHitRule** object when the site hit rule is created, updated, or deleted. A **SiteHitRule** object sets how many crawler sessions (threads) can simultaneously crawl the given site. 
  
If the **Identity** parameter is not specified, this cmdlet returns the site hit rule collection for the specified search application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SiteHitRulePipeBind  <br/> |Specifies the site hit rule to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh, or an instance of a valid **SiteHitRule** object.  <br/> |
| _SearchService_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServicePipeBind  <br/> |Specifies the search service that hosts the crawler with the specified shared site search rules.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SiteHitRulePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**SearchService** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServicePipeBind  <br/> ||
   

