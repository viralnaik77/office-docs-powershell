---
title: "New-SPEnterpriseSearchQueryScopeRule"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 2/11/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fbcd7080-339c-470d-8bed-2509c99df204

description: "The New-SPEnterpriseSearchQueryScopeRule cmdlet has been deprecated and will be removed in a future release."
---

# New-SPEnterpriseSearchQueryScopeRule

The **New-SPEnterpriseSearchQueryScopeRule** cmdlet has been deprecated and will be removed in a future release. 
  
Adds a shared scope rule to a query scope.
  
```
New-SPEnterpriseSearchQueryScopeRule -RuleType <String> -Scope <ScopePipeBind> -Url <Uri> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-FilterBehavior <String>] [-ManagedProperty <ManagedPropertyPipeBind>] [-MatchingString <String>] [-PropertyValue <String>] [-SearchApplication <SearchServiceApplicationPipeBind>] [-UrlScopeRuleType <String>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity
```

```
$scope = Get-SPEnterpriseSearchQueryScope -Identity MustCrawl -SearchApplication $ssa
```

```
$sr = New-SPEnterpriseSearchQueryScopeRule -Scope $scope -RuleType AllContent -Url http://criticalSite
```

```
Get-SPEnterpriseSearchQueryScopeRule -Scope $scope -Url http://criticalSite
```

This example creates a new scope rule of type  `AllContent` for the URL  `http://criticalSite`.
  
## Detailed Description

> [!NOTE]
> After you upgrade a Search service application from SharePoint Server 2010 to SharePoint Server 2013, you can view shared scopes, but you cannot create, update, or delete them. Therefore, you cannot use this cmdlet for shared scopes after upgrade. However, you can convert shared scopes to result sources, which serve a similar purpose. Similarly, after you upgrade a SharePoint Server 2010 site collection to SharePoint Server 2013 mode, you can view local scopes, but you cannot create, update, or delete them. Therefore, you cannot use this cmdlet for local scopes after you upgrade a site collection. However, you can convert local scopes to result sources, which serve a similar purpose. 
  
The **New-SPEnterpriseSearchQueryScopeRule** cmdlet creates a new shared scope rule. **SPEnterpriseSearchQueryScopeRule** represents a query results scope rule that can be applied to a scope. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _RuleType_ <br/> |Required  <br/> |System.String  <br/> |Specifies the type of scope rule to create.  <br/> The type must be one of the following values: **AllContent**, **Url**, or **PropertyQuery**.  <br/> |
| _Scope_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ScopePipeBind  <br/> |Applies the query scope rule to the specified scope.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a scope (for example, Scope1); or an instance of a valid **Scope** object.  <br/> |
| _Url_ <br/> |Required  <br/> |System.Uri  <br/> |Specifies the results URL that is associated with the query scope rule.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _FilterBehavior_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the type of scope rule to create for the query scope. The default value is **Include**.  <br/> The type must be one of the following values: **Exclude**, **Include**, or **Require**.  <br/> |
| _ManagedProperty_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ManagedPropertyPipeBind  <br/> |Specifies the managed property to use for the PropertyQuery scope rule.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a managed property (for example, ManagedProperty1); or an instance of a valid **ManagedProperty** object.  <br/> |
| _MatchingString_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the string to use when matching the URL rule type.  <br/> |
| _PropertyValue_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the property value to use when matching the PropertyQuery rule type.  <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the query scope rule collection.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _UrlScopeRuleType_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the value to use when matching the URL rule type.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**RuleType** <br/> |Required  <br/> |System.String  <br/> ||
|**Scope** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ScopePipeBind  <br/> ||
|**Url** <br/> |Required  <br/> |System.Uri  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**FilterBehavior** <br/> |Optional  <br/> |System.String  <br/> ||
|**ManagedProperty** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ManagedPropertyPipeBind  <br/> ||
|**MatchingString** <br/> |Optional  <br/> |System.String  <br/> ||
|**PropertyValue** <br/> |Optional  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**UrlScopeRuleType** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Remove-SPEnterpriseSearchQueryScopeRule](remove-spenterprisesearchqueryscoperule.md)
  
[Get-SPEnterpriseSearchQueryScopeRule](get-spenterprisesearchqueryscoperule.md)
  
[Set-SPEnterpriseSearchQueryScopeRule](set-spenterprisesearchqueryscoperule.md)
  
[Get-SPEnterpriseSearchQueryScope](get-spenterprisesearchqueryscope.md)

