---
title: "New-SPEnterpriseSearchQueryScope"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 2/11/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d466ffbc-daee-48a3-a376-9beb38f0fd26

description: "The New-SPEnterpriseSearchQueryScope cmdlet has been deprecated and will be removed in a future release."
---

# New-SPEnterpriseSearchQueryScope

The **New-SPEnterpriseSearchQueryScope** cmdlet has been deprecated and will be removed in a future release. 
  
Adds a query results scope to a shared search application.
  
```
New-SPEnterpriseSearchQueryScope -Description <String> -DisplayInAdminUI <$true | $false> -Name <String> -SearchApplication <SearchServiceApplicationPipeBind> [-AlternateResultsPage <String>] [-AssignmentCollection <SPAssignmentCollection>] [-CompilationType <Int32>] [-Confirm [<SwitchParameter>]] [-ExtendedSearchFilter <String>] [-OwningSiteUrl <Uri>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity MySSA$ssa | New-SPEnterpriseSearchQueryScope -Name MustCrawl -Description "Sites we must crawl" -DisplayInAdminUI $true
```

This example adds a scope named  `MustCrawl` that will be displayed in the administration UI to the search service application named  `MySSA`.
  
## Detailed Description

> [!NOTE]
> After you upgrade a Search service application from SharePoint Server 2010 to SharePoint Server 2013, you can view shared scopes, but you cannot create, update, or delete them. Therefore, you cannot use this cmdlet for shared scopes after upgrade. However, you can convert shared scopes to result sources, which serve a similar purpose. Similarly, after you upgrade a SharePoint Server 2010 site collection to SharePoint Server 2013 mode, you can view local scopes, but you cannot create, update, or delete them. Therefore, you cannot use this cmdlet for local scopes after you upgrade a site collection. However, you can convert local scopes to result sources, which serve a similar purpose. 
  
Use the **New-SPEnterpriseSearchQueryScope** cmdlet to create a new shared scope. **SPEnterpriseSearchQueryScope** represents a query results scope used by all shared search applications on the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Description_ <br/> |Required  <br/> |System.String  <br/> |Adds a description of the new query scope.  <br/> The type must be a valid string; for example, a description of a query scope.  <br/> |
| _DisplayInAdminUI_ <br/> |Required  <br/> |System.Boolean  <br/> |Specifies that the new scope is displayed in the administration application user interface (UI). The default setting is to hide the new scope in the administration application UI.  <br/> |
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the identity of the scope to create.  <br/> The type must be a valid name of a scope (for example, Scope1).  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the query scope collection.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AlternateResultsPage_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the location to display results for the new query scope.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CompilationType_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the compilation type of the new scope. The value **0** specifies the conditionally compiled scope type, and the value **1** specifies the always compiled scope type.  <br/> The type must be either of the following: **0** or **1**.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _ExtendedSearchFilter_ <br/> |Optional  <br/> |System.String  <br/> |PARAMVALUE: String  <br/> |
| _OwningSiteUrl_ <br/> |Optional  <br/> |System.Uri  <br/> |Specifies the SharePoint site that is associated with the new scope.  <br/> The type must be a valid SharePoint site URL, in the form http://server_name.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**Description** <br/> |Required  <br/> |System.String  <br/> ||
|**DisplayInAdminUI** <br/> |Required  <br/> |System.Nullable  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AlternateResultsPage** <br/> |Optional  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CompilationType** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ExtendedSearchFilter** <br/> |Optional  <br/> |System.String  <br/> ||
|**OwningSiteUrl** <br/> |Optional  <br/> |System.Uri  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchQueryScope](get-spenterprisesearchqueryscope.md)
  
[Set-SPEnterpriseSearchQueryScope](set-spenterprisesearchqueryscope.md)
  
[Remove-SPEnterpriseSearchQueryScope](remove-spenterprisesearchqueryscope.md)
  
[New-SPEnterpriseSearchQueryScopeRule](new-spenterprisesearchqueryscoperule.md)

