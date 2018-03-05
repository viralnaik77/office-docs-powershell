---
title: "Remove-SPEnterpriseSearchQueryScopeRule"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 2/11/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0f1de66-7272-4dc4-bf5e-408a5f11ef42

description: "The Remove-SPEnterpriseSearchQueryScopeRule cmdlet has been deprecated and will be removed in a future release."
---

# Remove-SPEnterpriseSearchQueryScopeRule

The **Remove-SPEnterpriseSearchQueryScopeRule** cmdlet has been deprecated and will be removed in a future release. 
  
Deletes query results scope rules.
  
```
Remove-SPEnterpriseSearchQueryScopeRule -Identity <ScopeRulePipeBind> -Url <Uri> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Scope <ScopePipeBind>] [-SearchApplication <SearchServiceApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "MySSA"
$scope = Get-SPEnterpriseSearchQueryScope -Identity MustCrawl -SearchApplication $ssa
Get-SPEnterpriseSearchQueryScopeRule -Scope $scope -Url http://criticalSite | Remove-SPEnterpriseSearchQueryScopeRule -Url http://criticalSite
```

This example removes a scope rule for the URL  `http://criticalSite` from a search service application named  `MySSA`.
  
## Detailed Description

> [!NOTE]
> After you upgrade a Search service application from SharePoint Server 2010 to SharePoint Server 2013, you can view shared scopes, but you cannot create, update, or delete them. Therefore, you cannot use this cmdlet for shared scopes after upgrade. However, you can convert shared scopes to result sources, which serve a similar purpose. Similarly, after you upgrade a SharePoint Server 2010 site collection to SharePoint Server 2013 mode, you can view local scopes, but you cannot create, update, or delete them. Therefore, you cannot use this cmdlet for local scopes after you upgrade a site collection. However, you can convert local scopes to result sources, which serve a similar purpose. 
  
The **Remove-SPEnterpriseSearchQueryScopeRule** cmdlet deletes one or more shared scope rules from the scope rule collection. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ScopeRulePipeBind  <br/> |Specifies the scope rule to delete.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a scope rule (for example, ScopeRule1); or an instance of a valid **ScopeRule** object.  <br/> |
| _Url_ <br/> |Required  <br/> |System.Uri  <br/> |Filters to delete query scope rules for the specified results URL.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Scope_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ScopePipeBind  <br/> |Filters to delete multiple rules for a specified scope.  <br/> The type must be a valid string that identifies the scope; for example, Scope1.  <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the query scope rule collection.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ScopeRulePipeBind  <br/> ||
|**Url** <br/> |Required  <br/> |System.Uri  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Scope** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ScopePipeBind  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchQueryScopeRule](get-spenterprisesearchqueryscoperule.md)
  
[New-SPEnterpriseSearchQueryScopeRule](new-spenterprisesearchqueryscoperule.md)
  
[Set-SPEnterpriseSearchQueryScopeRule](set-spenterprisesearchqueryscoperule.md)
  
[Get-SPEnterpriseSearchQueryScope](get-spenterprisesearchqueryscope.md)

