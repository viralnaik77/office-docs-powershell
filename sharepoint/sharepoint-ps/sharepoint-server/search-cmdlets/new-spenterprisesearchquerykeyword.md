---
title: "New-SPEnterpriseSearchQueryKeyword"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 57a4e37e-462a-4b1b-8bea-39fcfe9ed34e

description: "Adds a keyword term to a shared search application."
---

# New-SPEnterpriseSearchQueryKeyword

Adds a keyword term to a shared search application.
  
```
New-SPEnterpriseSearchQueryKeyword -Site <SPSitePipeBind> -Term <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Contact <String>] [-Definition <String>] [-EndDate <DateTime>] [-ReviewDate <DateTime>] [-StartDate <DateTime>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
New-SPEnterpriseSearchQueryKeyword -Term Tangible -Site http://myserver/sites/team
```

This example creates a new query keyword for the site  `http://myserver/sites/team` with the term  `Tangible`.
  
## Detailed Description

The **New-SPEnterpriseSearchQueryKeyword** cmdlet changes query results by creating a new keyword. A query keyword is a query component of a query topology. **SPEnterpriseSearchQueryKeyword** represents relevance setting through keywords. 
  
> [!NOTE]
> You can use this cmdlet for keywords in site collections that are in SharePoint Server 2010 mode. You cannot use this cmdlet after a site collection is upgraded to SharePoint Server 2013 mode because keywords and Best Bets are automatically migrated to query rules. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Site_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Associates the new keyword term to the specified results URL.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL, in the form http://server_name; or an instance of a valid **SPSite** object.  <br/> |
| _Term_ <br/> |Required  <br/> |System.String  <br/> |Specifies the keyword term to create.  <br/> The type must be a valid string that contains a keyword term (for example, KeywordTerm1).  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Contact_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the user name associated with the new keyword.  <br/> The type must be a valid user name; for example, KeywordUser1.  <br/> |
| _Definition_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the definition of the new keyword term.  <br/> The type must be a valid string; for example, a keyword term definition.  <br/> |
| _EndDate_ <br/> |Optional  <br/> |System.DateTime  <br/> |Specifies the expiration date of the keyword term. The default value is **MaxDate**.  <br/> The type must be a valid **DateTime** type, in the form 2010,12,05.  <br/> |
| _ReviewDate_ <br/> |Optional  <br/> |System.DateTime  <br/> |Specifies the review date of the keyword term. The default value is **MaxDate**.  <br/> The type must be a valid date, in the form 2010,12,05.  <br/> |
| _StartDate_ <br/> |Optional  <br/> |System.DateTime  <br/> |Specifies the activation date for the keyword term. The default value is the current date.  <br/> The type must be a valid date, in the form 2010,12,05.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Term** <br/> |Required  <br/> |System.String  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Contact** <br/> |Optional  <br/> |System.String  <br/> ||
|**Definition** <br/> |Optional  <br/> |System.String  <br/> ||
|**EndDate** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**ReviewDate** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**StartDate** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchQueryKeyword](get-spenterprisesearchquerykeyword.md)
  
[Set-SPEnterpriseSearchQueryKeyword](set-spenterprisesearchquerykeyword.md)
  
[Remove-SPEnterpriseSearchQueryKeyword](remove-spenterprisesearchquerykeyword.md)

