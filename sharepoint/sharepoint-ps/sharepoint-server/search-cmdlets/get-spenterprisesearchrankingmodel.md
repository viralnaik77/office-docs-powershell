---
title: "Get-SPEnterpriseSearchRankingModel"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86e09226-2821-4c28-83a4-c4d5dd496222

description: "Returns a ranking model."
---

# Get-SPEnterpriseSearchRankingModel

Returns a ranking model.
  
```
Get-SPEnterpriseSearchRankingModel -Owner <SearchObjectOwner> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <RankingModelPipeBind>]

```

## Example

------------------EXAMPLE 1------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "Search Service Application"
```

```
$owner = Get-SPEnterpriseSearchOwner -Level ssa
```

```
Get-SPEnterpriseSearchRankingModel -Identity 8f6fd0bc-06f9-43cf-bbab-08c377e083f4 -SearchApplication $ssa -Owner $owner
```

This example retrieves the ranking model on the  `search service application` level with the identity  `8f6fd0bc-06f9-43cf-bbab-08c377e083f4` for the search application  `Search Service Application`.
  
------------------EXAMPLE 2------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "Search Service Application"
```

```
$owner = Get-SPEnterpriseSearchOwner -Level ssa
```

```
Get-SPEnterpriseSearchRankingModel -SearchApplication $ssa -Owner $owner
```

This example retrieves all ranking models defined on the  `search service application` level for the search application  `Search Service Application`.
  
## Detailed Description

This cmdlet reads the **RankingModel** object when a ranking model is created, removed, or updated. 
  
If the **Identity** parameter is not specified or the identity does not match any of the ranking models in the collection, all rank models for the search application are returned. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Owner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the scope where the ranking model is available. The available scopes are: SSA, Tenant, Site Collection or Site. A ranking model can be available in multiple scopes.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the ranking model.  <br/> The type must be a valid GUID in the form 9bf36458-fc99-4f7b-b060-867e5a63adce, a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.RankingModelPipeBind  <br/> |Specifies the ranking model to retrieve.  <br/> The type must be a valid GUID in the form 8f6fd0bc-06f9-43cf-bbab-08c377e083f4, or an instance of a valid **RankingModel** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.RankingModelPipeBind  <br/> ||
|**Owner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchRankingModel](new-spenterprisesearchrankingmodel.md)
  
[Set-SPEnterpriseSearchRankingModel](set-spenterprisesearchrankingmodel.md)
  
[Remove-SPEnterpriseSearchRankingModel](remove-spenterprisesearchrankingmodel.md)

