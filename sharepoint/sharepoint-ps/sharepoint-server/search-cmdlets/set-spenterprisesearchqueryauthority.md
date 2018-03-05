---
title: "Set-SPEnterpriseSearchQueryAuthority"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4985f5e3-c922-45cb-b964-ec169e93f56c

description: "Sets the properties of an authoritative page for a shared search application."
---

# Set-SPEnterpriseSearchQueryAuthority

Sets the properties of an authoritative page for a shared search application.
  
```
Set-SPEnterpriseSearchQueryAuthority -Identity <AuthorityPagePipeBind> -Owner <SearchObjectOwner> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Level <Single>] [-SearchApplication <SearchServiceApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
Set-SPEnterpriseSearchQueryAuthority -Identity http://contoso.com -Level 0.5 -SearchApplication MySSA
```

This example adjusts the authoritative level of the URL  `http://contoso.com` to  `0.5` on the search service application named  `MySSA`.
  
## Detailed Description

The **Set-SPEnterpriseSearchQueryAuthority** cmdlet updates properties of an authoritative page and adjusts the query rank of an authoritative page. **SPEnterpriseSearchQueryAuthority** represents authoritative sites that rank higher in relevance than demoted sites, which are de-emphasized in relevance. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.AuthorityPagePipeBind  <br/> |Specifies the query authority page to update.  <br/> The type must be a valid URL, in the form http://server_name; or an instance of a valid **AuthorityPage** object.  <br/> |
| _Owner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the search object owner that defines the scope at which the corresponding **Query Authority** is created.The owner must be one of the following valid levels:- Search Service Application- Site Subscription  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Level_ <br/> |Optional  <br/> |System.Single  <br/> |Specifies the level of the new authoritative page. Authoritative pages, designated by the service application administrator, are expert pages that link to the most relevant information. Because a search service application can have several designated authoritative pages, you use the **Level** property to specify the value of a specific page. This parameter sets the level for the most valuable authoritative pages to **0**.  <br/> The type must be one of the following floating-point numbers: 0, 1, or 2.  <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the authority page collection.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.AuthorityPagePipeBind  <br/> ||
|**Owner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Level** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchQueryAuthority](new-spenterprisesearchqueryauthority.md)
  
[Get-SPEnterpriseSearchQueryAuthority](get-spenterprisesearchqueryauthority.md)
  
[Remove-SPEnterpriseSearchQueryAuthority](remove-spenterprisesearchqueryauthority.md)

