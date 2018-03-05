---
title: "New-SPEnterpriseSearchQueryAuthority"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 81be139d-d4ed-4390-b782-292fc9b15637

description: "Adds an authoritative page to a shared search application."
---

# New-SPEnterpriseSearchQueryAuthority

Adds an authoritative page to a shared search application.
  
```
New-SPEnterpriseSearchQueryAuthority -Level <Single> -Owner <SearchObjectOwner> -SearchApplication <SearchServiceApplicationPipeBind> -Url <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplicationNew-SPEnterpriseSearchQueryAuthority -SearchApplication $ssa -Url http://contoso.com -Level 1.5
```

This example designates the URL `http://contoso.com` as an authoritative page with a relative importance of 1.5. 
  
## Detailed Description

The **New-SPEnterpriseSearchQueryAuthority** cmdlet adds an authoritative page to adjust query rank. **SPEnterpriseSearchQueryAuthority** represents authoritative sites that rank higher in relevance than demoted sites, which are de-emphasized in relevance. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Level_ <br/> |Required  <br/> |System.Single  <br/> |Specifies the level of the new authoritative page. Authoritative pagesare expert pages that link to the most relevant information. A search service application can have multiple authoritative pages. The **Level** property is used to specify the relative relevance adjustment of the authoritative pages. This parameter may receive a floating point value of 0.0 - 2.0, where 0.0 has the most positive impact on relevance.  <br/> |
| _Owner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the search object owner that defines the scope at which the corresponding **Query Authority** is created.The owner must be one of the following valid levels:- Search Service Application- Site Subscription  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the authority page collection.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _Url_ <br/> |Required  <br/> |System.String  <br/> |Specifies the query authority page to create.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Url** <br/> |Required  <br/> |System.String  <br/> ||
|**Level** <br/> |Required  <br/> |System.Single  <br/> ||
|**Owner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchQueryAuthority](get-spenterprisesearchqueryauthority.md)
  
[Set-SPEnterpriseSearchQueryAuthority](set-spenterprisesearchqueryauthority.md)
  
[Remove-SPEnterpriseSearchQueryAuthority](remove-spenterprisesearchqueryauthority.md)

