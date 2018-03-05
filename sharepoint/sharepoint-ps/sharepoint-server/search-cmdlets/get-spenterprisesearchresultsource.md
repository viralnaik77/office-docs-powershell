---
title: "Get-SPEnterpriseSearchResultSource"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9cc5400-3c42-4fbe-b7bb-d65cf47bf448

description: "Retrieves a result source."
---

# Get-SPEnterpriseSearchResultSource

Retrieves a result source.
  
```
Get-SPEnterpriseSearchResultSource -Owner <SearchObjectOwner> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <ResultSourcePipeBind>]

```

## Example

------------------EXAMPLE 1------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "Search Service Application"
```

```
$owner = Get-SPEnterpriseSearchOwner -Level SSA
```

```
Get-SPEnterpriseSearchResultSource -Identity "Local SharePoint Results" -SearchApplication $ssa -Owner $owner
```

This example retrieves the search service application level result source with the name "Local SharePoint Results".
  
------------------EXAMPLE 2---------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "Search Service Application"
```

```
$owner = Get-SPEnterpriseSearchOwner -Level SSA
```

```
Get-SPEnterpriseSearchResultSource -Identity 8413cd39-2156-4e00-b54d-11efd9abdB89 -SearchApplication $ssa -Owner $owner
```

This example retrieves the search service application level result source with the id 8413cd39-2156-4e00-b54d-11efd9abdB89.
  
------------------EXAMPLE 3------------------
  
```
C:\PS>$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "Search Service Application"
$owner = Get-SPEnterpriseSearchOwner -Level SSA
```

```
Get-SPEnterpriseSearchResultSource -SearchApplication $ssa -Owner $owner
```

This example retrieves all the search service application level result sources.
  
## Detailed Description

This cmdlet retrieves a result source object. If the Identity parameter is not specified, this cmdlet returns the result source collection for the specified search object owner.
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Owner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the search object owner that defines the scope at which the corresponding result source is available.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ResultSourcePipeBind  <br/> |Specifies the result source to retrieve. The type must be a valid GUID string, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a result source (for example, "Local SharePoint Results"); or an instance of a valid **Source** object. If not specified, the result source collection for the specified search object owner is returned.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ResultSourcePipeBind  <br/> ||
|**Owner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchResultSource](new-spenterprisesearchresultsource.md)
  
[Set-SPEnterpriseSearchResultSource](set-spenterprisesearchresultsource.md)
  
[Remove-SPEnterpriseSearchResultSource](remove-spenterprisesearchresultsource.md)

