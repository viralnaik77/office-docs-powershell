---
title: "Get-SPEnterpriseSearchQueryAuthority"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2ba641eb-34f9-4026-a350-543fd7787aa5

description: "Returns an authoritative page."
---

# Get-SPEnterpriseSearchQueryAuthority

Returns an authoritative page.
  
```
Get-SPEnterpriseSearchQueryAuthority -Owner <SearchObjectOwner> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <AuthorityPagePipeBind>]

```

## Example

------------------EXAMPLE 1------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "MySSA"$qAuth = $ssa | Get-SPEnterpriseSearchQueryAuthority -Identity "http://contoso.com"
```

This example obtains the authoritative page for the URL  `http://contoso.com` from the search service application named  `MySSA`.
  
------------------EXAMPLE 2------------------
  
```
$qaCollection = Get-SPEnterpriseSearchQueryAuthority -SearchApplication "MySSA"
```

This example obtains the collection of query authority pages from a search service application named  `MySSA`.
  
## Detailed Description

The **Get-SPEnterpriseSearchQueryAuthority** cmdlet reads a **QueryAuthority** object when the authoritative page is created or deleted or when the query rank is modified. 
  
If the **Identity** parameter is not specified, this cmdlet returns the authority page collection for the specified search application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Owner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the search object owner that defines the scope at which the corresponding **Query Authority** is created.The owner must be one of the following valid levels:- Search Service Application- Site Subscription  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the authority page to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.AuthorityPagePipeBind  <br/> |Specifies the query authority to get.  <br/> The type must be a valid URL, in the form http://server_name; or an instance of a valid **AuthorityPage** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.AuthorityPagePipeBind  <br/> ||
|**Owner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchQueryAuthority](new-spenterprisesearchqueryauthority.md)
  
[Set-SPEnterpriseSearchQueryAuthority](set-spenterprisesearchqueryauthority.md)
  
[Remove-SPEnterpriseSearchQueryAuthority](remove-spenterprisesearchqueryauthority.md)

