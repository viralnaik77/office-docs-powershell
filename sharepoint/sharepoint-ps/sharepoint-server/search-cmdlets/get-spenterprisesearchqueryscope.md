---
title: "Get-SPEnterpriseSearchQueryScope"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 2/11/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 228495d6-4716-4627-b46f-2b85eaa8edbc

description: "The Get-SPEnterpriseSearchQueryScope cmdlet has been deprecated, and will be removed in a future release."
---

# Get-SPEnterpriseSearchQueryScope

The **Get-SPEnterpriseSearchQueryScope** cmdlet has been deprecated, and will be removed in a future release. 
  
Returns a query results scope.
  
```
Get-SPEnterpriseSearchQueryScope -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <ScopePipeBind>] [-Url <Uri>]

```

## Example

------------------EXAMPLE------------------
  
```
$ssa = Get-SPenterpriseSearchServiceApplication -Identity MySSA
Get-SPEnterpriseSearchQueryScope -Identity MustCrawl -SearchApplication $ssa | Set-SPEnterpriseSearchQueryScope -Description "Business critical sites to index" -CompilationType 1 -AlternateResultsPage http://altServer
```

This example obtains a reference to the scope named  `MustCrawl` on the search application named  `MySSA`, and changes the description, compilation type, and alternate access URL.
  
## Detailed Description

The **Get-SPEnterpriseSearchQueryScope** cmdlet reads a **QueryScope** object when the shared scope is created or deleted, or when the definition of the shared scope is updated. 
  
If the **Identity** parameter is not specified, this cmdlet returns the query scope collection from the specified search application. 
  
> [!NOTE]
> In SharePoint Server 2013, result sources provide the functionality that scopes provided in SharePoint Server 2010. > During an upgrade from SharePoint Server 2010, to retain legacy settings, shared scopes are automatically migrated. However, these scopes are read-only after the migration. This cmdlet can be used to read a shared scope that has been migrated. > During an upgrade from SharePoint Server 2010, to preserve legacy settings, local scopes are also automatically migrated when the corresponding sites or site collections are migrated. In a SharePoint Server 2013 farm, the scopes of a site or site collection that is in SharePoint Server 2010 mode are read-write, whereas the scopes of a site or site collection after upgrade to SharePoint Server 2013 mode are read-only. This cmdlet can be used to read a migrated local scope in either situation. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the query scope.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ScopePipeBind  <br/> |Specifies the results scope to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a scope (for example, Scope1); or an instance of a valid **Scope** object.  <br/> |
| _Url_ <br/> |Optional  <br/> |System.Uri  <br/> |Filters to return scopes for the specified results URL.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ScopePipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Url** <br/> |Optional  <br/> |System.Uri  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchQueryScope](new-spenterprisesearchqueryscope.md)
  
[Set-SPEnterpriseSearchQueryScope](set-spenterprisesearchqueryscope.md)
  
[Remove-SPEnterpriseSearchQueryScope](remove-spenterprisesearchqueryscope.md)
  
[New-SPEnterpriseSearchQueryScopeRule](new-spenterprisesearchqueryscoperule.md)

