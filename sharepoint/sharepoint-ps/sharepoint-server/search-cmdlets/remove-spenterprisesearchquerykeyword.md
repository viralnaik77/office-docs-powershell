---
title: "Remove-SPEnterpriseSearchQueryKeyword"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0967401b-8688-48cc-bbec-cd4dea8f5f3b

description: "Deletes a query keyword."
---

# Remove-SPEnterpriseSearchQueryKeyword

Deletes a query keyword.
  
```
Remove-SPEnterpriseSearchQueryKeyword -Identity <KeywordPipeBind> -Site <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
Get-SPEnterpriseSearchQueryKeyword -Identity Engineering -Site http://myserver/sites/engineering | Remove-SPEnterpriseSearchQueryKeyword -Site http://myserver/sites/engineering
```

This example removes the  `Engineering` keyword from the site collection at  `http://myserver/sites/engineering`.
  
## Detailed Description

The **Remove-SPEnterpriseSearchQueryKeyword** cmdlet deletes unused or unwanted keywords from the query keyword collection. 
  
> [!NOTE]
> You can use this cmdlet for keywords in site collections that are in SharePoint Server 2010 mode. You cannot use this cmdlet after a site collection is upgraded to SharePoint Server 2013 mode because keywords and Best Bets are automatically migrated to query rules. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.KeywordPipeBind  <br/> |Specifies the keyword term to delete.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid string that contains a keyword term (for example, KeywordTerm1); or an instance of a valid **Keyword** object.  <br/> |
| _Site_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Filters to delete keywords from the specified site collection of results.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL, in the form http://server_name; or an instance of a valid **SPSite** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.KeywordPipeBind  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchQueryKeyword](get-spenterprisesearchquerykeyword.md)
  
[New-SPEnterpriseSearchQueryKeyword](new-spenterprisesearchquerykeyword.md)
  
[Set-SPEnterpriseSearchQueryKeyword](set-spenterprisesearchquerykeyword.md)

