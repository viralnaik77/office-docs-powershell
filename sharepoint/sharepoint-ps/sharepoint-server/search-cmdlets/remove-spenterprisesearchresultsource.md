---
title: "Remove-SPEnterpriseSearchResultSource"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa7f0dfe-cbda-4962-81b1-14174c249822

description: "Deletes a result source."
---

# Remove-SPEnterpriseSearchResultSource

Deletes a result source.
  
```
Remove-SPEnterpriseSearchResultSource -Identity <ResultSourcePipeBind> -Owner <SearchObjectOwner> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

--------EXAMPLE1 --------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "Search Service Application"
```

```
$owner = Get-SPEnterpriseSearchOwner -Level SSA
```

```
Remove-SPEnterpriseSearchResultSource -Identity "Custom SharePoint Result Source" -SearchApplication $ssa -Owner $owner
```

This example deletes the search service application level result source with the name "Custom SharePoint Result Source".
  
--------EXAMPLE 2 --------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "Search Service Application"
```

```
$owner = Get-SPEnterpriseSearchOwner -Level SSA
```

```
Remove-SPEnterpriseSearchResultSource -Identity 12345678-90ab-cdef-1234-567890bcdefgh -SearchApplication $ssa -Owner $owner
```

This example deletes the search service application level result source with the id 12345678-90ab-cdef-1234-567890bcdefgh.
  
--------EXAMPLE 3 --------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "Search Service Application"
```

```
$owner = Get-SPEnterpriseSearchOwner -Level SSA
```

```
$resultSource = Get-SPEnterpriseSearchResultSource -Identity "Custom SharePoint Result Source" -SearchApplication $ssa -Owner $owner
```

```
Remove-SPEnterpriseSearchResultSource -Identity $resultSource -SearchApplication $ssa -Owner $owner
```

This example deletes the search service application level result source with the name "Custom SharePoint Result Source", by specifying a Source instance.
  
## Detailed Description

This cmdlet deletes a specified result source. This cmdlet supports the same delete operations as are supported through the "Manage Result Sources" page in the SharePoint Central Administration website. The result source cannot be a built-in source (a built-in source has the **BuiltIn** property set to true). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ResultSourcePipeBind  <br/> |Specifies the result source to delete. The type must be a valid GUID string, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a result source (for example, "Custom SharePoint Result Source"); or an instance of a valid **Source** object.  <br/> |
| _Owner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the search object owner and its level to retrieve result source.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ResultSourcePipeBind  <br/> ||
|**Owner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchResultSource](new-spenterprisesearchresultsource.md)
  
[Set-SPEnterpriseSearchResultSource](set-spenterprisesearchresultsource.md)
  
[Get-SPEnterpriseSearchResultSource](get-spenterprisesearchresultsource.md)

