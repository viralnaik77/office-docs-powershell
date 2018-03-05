---
title: "New-SPEnterpriseSearchRankingModel"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80fdbeb4-356f-4212-8798-ef99839e94ce

description: "Adds a ranking model to a shared search application."
---

# New-SPEnterpriseSearchRankingModel

Adds a ranking model to a shared search application.
  
```
New-SPEnterpriseSearchRankingModel -Owner <SearchObjectOwner> -RankingModelXML <String> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "Search Service Application"
```

```
$owner = Get-SPEnterpriseSearchOwner -Level SPWeb -SPWeb http://sharepoint/team

```

```
$rankmodel = Get-Content .\rankModel.xml$rankmodel = [String]$rankmodel

```

```
New-SPEnterpriseSearchRankingModel -SearchApplication $ssa -Owner $owner -RankingModelXML $rankmodel
```

This example creates a ranking model for the site  `http://sharepoint/team` for the search service application  `Search Service Application` from the file  `rankModel.xml` which is stored in the current directory. 
  
## Detailed Description

This cmdlet adds a new ranking model to the assignment collection. The name, description, and identifier (ID) for the new ranking model are contained in the .xml file specified in **RankingModelXML**. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Owner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the scope where the ranking model is available. The available scopes are: SSA, Tenant, Site Collection or Site. A ranking model can be available in multiple scopes.  <br/> |
| _RankingModelXML_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the XML representation of the new ranking model.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the ranking model.  <br/> The type must be a valid GUID in the 9bf36458-fc99-4f7b-b060-867e5a63adce, a valid search application name (for example, SearchApp1), or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Owner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**RankingModelXML** <br/> |Required  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchRankingModel](get-spenterprisesearchrankingmodel.md)
  
[Set-SPEnterpriseSearchRankingModel](set-spenterprisesearchrankingmodel.md)
  
[Remove-SPEnterpriseSearchRankingModel](remove-spenterprisesearchrankingmodel.md)

