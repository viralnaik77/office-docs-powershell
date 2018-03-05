---
title: "Set-SPEnterpriseSearchRankingModel"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67e3898f-1232-4149-9edd-eab8ba8cdc57

description: "Sets the properties of a ranking model for a shared search service application."
---

# Set-SPEnterpriseSearchRankingModel

Sets the properties of a ranking model for a shared search service application.
  
```
Set-SPEnterpriseSearchRankingModel -Identity <RankingModelPipeBind> -Owner <SearchObjectOwner> -RankingModelXML <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-SearchApplication <SearchServiceApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "Search Service Application"
```

```
$owner = Get-SPEnterpriseSearchOwner -Level ssa
```

```
$rankingModel = Get-SPEnterpriseSearchRankingModel -Identity 8f6fd0bc-06f9-43cf-bbab-08c377e083f4 -SearchApplication $ssa -Owner $owner
```

```
$newrankmodel = Get-Content .\newRankModel.xml$newrankmodel = [String]$newrankmodel
```

```
Set-SPEnterpriseSearchRankingModel -Identity $rankingModel -SearchApplication $ssa -Owner $owner -RankingModelXML $newrankmodel
```

This example reconfigures the ranking model with the identity  `8f6fd0bc-06f9-43cf-bbab-08c377e083f4` with the new ranking model specified in  `newRankModel.xml`.
  
## Detailed Description

This cmdlet updates properties of a ranking model for a search service application. The name, description, and identifier (ID) for a ranking model are contained in the .xml file specified in **RankingModelXML**. If the **Identity** parameter is not specified or the identity does not match any of the ranking models in the collection, an exception is thrown and the default ranking model is used. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.RankingModelPipeBind  <br/> |Specifies the ranking model to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh, or an instance of a valid **RankingModel** object.  <br/> |
| _Owner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the scope where the ranking model is available. The available scopes are: SSA, Tenant, Site Collection or Site. A ranking model can be available in multiple scopes.  <br/> |
| _RankingModelXML_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the XML representation of the new ranking model.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the ranking model.  <br/> The type must be a valid GUID in the 9bf36458-fc99-4f7b-b060-867e5a63adce, a valid search application name (for example, SearchApp1), or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.RankingModelPipeBind  <br/> ||
|**Owner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**RankingModelXML** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchRankingModel](new-spenterprisesearchrankingmodel.md)
  
[Get-SPEnterpriseSearchRankingModel](get-spenterprisesearchrankingmodel.md)
  
[Remove-SPEnterpriseSearchRankingModel](remove-spenterprisesearchrankingmodel.md)

