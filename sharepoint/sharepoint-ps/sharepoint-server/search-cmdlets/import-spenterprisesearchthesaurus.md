---
title: "Import-SPEnterpriseSearchThesaurus"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eb1fdf2f-324d-4023-b534-93664b45d17d

description: "Deploys the dictionary to the thesaurus component in the query processing flow."
---

# Import-SPEnterpriseSearchThesaurus

Deploys the dictionary to the thesaurus component in the query processing flow.
  
```
Import-SPEnterpriseSearchThesaurus -FileName <String> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE-----------------
  
```
$searchApp = Get-SPEnterpriseSearchServiceApplication

```

```
Import-SPEnterpriseSearchThesaurus -SearchApplication $searchApp -Filename \\host\share\thesaurus.csv
```

This example imports a thesaurus dictionary .cvs file named  `thesaurus.csv` that is located at  `\\host\share` to the default search service application. 
  
## Detailed Description

This cmdlet imports a thesaurus dictionary using a .cvs file, and deploys it to the query processing flow. A previously deployed thesaurus is overwritten by an import of a new .cvs file. 
  
NOTE: If an empty .cvs file is imported, an empty thesaurus will be deployed. No synonyms will then be added to the queries.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _FileName_ <br/> |Required  <br/> |System.String  <br/> |Specifies the full UNC (Universal Naming Convention) path of the .cvs file to be imported.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application to which the thesaurus dictionary should be imported  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**FileName** <br/> |Required  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchServiceApplication](get-spenterprisesearchserviceapplication.md)

