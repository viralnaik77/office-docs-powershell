---
title: "Remove-SPEnterpriseSearchResultItemType"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 374da73e-a3aa-4560-b1ad-c771bafe155d

description: "Removes a result item type for a search object owner."
---

# Remove-SPEnterpriseSearchResultItemType

Removes a result item type for a search object owner.
  
```
Remove-SPEnterpriseSearchResultItemType -Identity <ResultItemTypePipeBind> -Owner <SearchObjectOwner> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-SearchApplication <SearchServiceApplicationPipeBind>] [-SearchApplicationProxy <SearchServiceApplicationProxyPipeBind>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------EXAMPLE--------
  
```
$web = Get-SPWeb "UrlOfTheSite"
```

```
$tenantOwner = Get-SPEnterpriseSearchOwner -Level SPSite -SPWeb $web
```

```
$searchapp = Get-SPEnterpriseSearchServiceApplication
```

```
$resultType = Get-SPEnterpriseSearchResultItemType -Owner $tenantOwner -SearchApplication $searchapp
```

```
$resultType.BuiltIn

```

```
Remove-SPEnterpriseSearchResultItemType -Identity $resultType -Owner $tenantOwner -SearchApplication $searchapp
```

This example first defines variables for the URL of the site, the search owner, and search application. It then retrieves the result item type and checks whether the result item type is a built-in result item type or not. If  `$resultType.BuiltIn` returns false, the result item type is not built-in and you can modify it. Next, the example removes the result item type referenced by **$resultType** for the owner referenced by **$tenantOwner**. 
  
## Detailed Description

The **Remove-SPEnterpriseSearchResultItemType** cmdlet removes a user-created result item type, given a result type identity and a search owner. You cannot use this cmdlet to remove the built-in result item types that are included with SharePoint products. 
  
Result item types enable you to change the look of search results based on the type of result. You start by defining a collection of rules, which will be evaluated against the properties of results. Then you define the display template to use for rendering that type of result. Once you have created the result item type, results matching the rules of the result item type will display using the specified display template.
  
Example use cases:
  
- Change the look of results for a particular file name extension, for example Word documents.
  
- Change the look of a particular content type in search results.
  
- Change the look of results from a particular author.
  
- Add a result action to results from a particular result source as part of a custom search application.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ResultItemTypePipeBind  <br/> |Specifies the result item type to update. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _Owner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the search object owner that defines the scope at which the result item type is created.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the name of the search application. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _SearchApplicationProxy_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationProxyPipeBind  <br/> |Specifies the proxy of the search application that contains the result item type. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application proxy name (for example, SearchAppProxy1); or an instance of a valid **SearchServiceApplicationProxy** object.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ResultItemTypePipeBind  <br/> ||
|**Owner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**SearchApplicationProxy** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationProxyPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchResultItemType](new-spenterprisesearchresultitemtype.md)
  
[Set-SPEnterpriseSearchResultItemType](set-spenterprisesearchresultitemtype.md)
  
[Get-SPEnterpriseSearchResultItemType](get-spenterprisesearchresultitemtype.md)
  
[Get-SPEnterpriseSearchOwner](get-spenterprisesearchowner.md)

