---
title: "Get-SPEnterpriseSearchQueryKeyword"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0dcc571f-cc53-4838-9f32-cf0baab4306f

description: "Returns a keyword term."
---

# Get-SPEnterpriseSearchQueryKeyword

Returns a keyword term.
  
```
Get-SPEnterpriseSearchQueryKeyword -Site <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <KeywordPipeBind>]

```

## Example

------------------EXAMPLE------------------
  
```
Get-SPEnterpriseSearchQueryKeyword -Identity Engineering -Site http://myserver/sites/engineering | Set-SPEnterpriseSearchQueryKeyword -StartDate "12/25/2009" -EndDate "12/24/2010" -Site http://myserver/sites/engineering
```

This example gets a reference to the keyword with the term  `Engineering` from the site  `http://myserver/sites/engineering` and sets the start dates and end dates for the keyword. 
  
## Detailed Description

The **Get-SPEnterpriseSearchQueryKeyword** cmdlet reads a **QueryKeyword** object when the keyword rule is created, updated, or deleted. 
  
If the **Identity** parameter is not specified, this cmdlet returns the query keyword collection from the specified search application. 
  
> [!NOTE]
> You can use this cmdlet for keywords in site collections that are in SharePoint Server 2010 mode. You cannot use this cmdlet after a site collection is upgraded to SharePoint Server 2013 mode because keywords and Best Bets are automatically migrated to query rules. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Site_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Filters to return keywords with the specified results URL.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL, in the form http://server_name; or an instance of a valid **SPSite** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.KeywordPipeBind  <br/> |Specifies the keyword term to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid string that contains a keyword term (for example, KeywordTerm1); or an instance of a valid **Keyword** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.KeywordPipeBind  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchQueryKeyword](new-spenterprisesearchquerykeyword.md)
  
[Set-SPEnterpriseSearchQueryKeyword](set-spenterprisesearchquerykeyword.md)
  
[Remove-SPEnterpriseSearchQueryKeyword](remove-spenterprisesearchquerykeyword.md)

