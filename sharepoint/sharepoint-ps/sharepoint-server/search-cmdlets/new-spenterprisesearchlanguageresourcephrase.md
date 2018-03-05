---
title: "New-SPEnterpriseSearchLanguageResourcePhrase"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c1a18869-1996-4a36-9f1e-884d158ddc0b

description: "Adds a language resource phrase to a shared search application."
---

# New-SPEnterpriseSearchLanguageResourcePhrase

Adds a language resource phrase to a shared search application.
  
```
New-SPEnterpriseSearchLanguageResourcePhrase -Language <String> -Name <String> -Owner <SearchObjectOwner> -SearchApplication <SearchServiceApplicationPipeBind> -Type <Undefined | QuerySuggestionBlockList | QuerySuggestionAlwaysSuggest | SpellingSuggestionBlockList | SummaryNoiseList | Nickname | LastNameMap | FirstNameMap | SpellingSuggestionAlwaysSuggest | CharacterMap | QuerySuggestionSubstitution> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Mapping <String>] [-SourceId <Guid>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication "SearchApp1"New-SPEnterpriseSearchLanguageResourcePhrase -SearchApplication $searchapp -Language en-us -Type QuerySuggestionBlockList -Name secret
```

This example adds a new entry to the  `QuerySuggestionBlockList` for the en-us language. 
  
## Detailed Description

The **New-SPEnterpriseSearchLanguageResourcePhrase** cmdlet adds a query keyword phrase to a shared search application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Language_ <br/> |Required  <br/> |System.String  <br/> |Adds the phrase for the specified source language.  <br/> The type must be a valid name of a language; for example, en-us or ja-jp.  <br/> |
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the term to add to the list specified in the **Type** parameter.  <br/> The type must be a valid name of a language resource phrase (for example, LanguageResourcePhrase1).  <br/> |
| _Owner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the search object owner that defines the scope at which the corresponding **LanguageResourcePhrase** is created.  <br/> The owner must be one of the following valid levels:  <br/> - Search Service Application  <br/> - Site Subscription  <br/> - Site Collection  <br/> - Site  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the language resources.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _Type_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.LanguageResourceType  <br/> |Specifies the type of the new phrase.  <br/> The type must be one of the following valid types of phrases:  <br/> - QuerySuggestionBlockList  <br/> - QuerySuggestionAlwaysSuggest  <br/> - Nickname  <br/> - QuerySuggestionSubstitution  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Mapping_ <br/> |Optional  <br/> |System.String  <br/> |Allows a term or phrase to be mapped to another term or phrase. For example, the nickname "John" could be mapped to "Jonathan".  <br/> This parameter only applies to nicknames and substitutions.  <br/> |
| _SourceId_ <br/> |Optional  <br/> |System.Guid  <br/> |Identifies the search result source for which the **LanguageResourcePhrase** applies to.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**Language** <br/> |Required  <br/> |System.String  <br/> ||
|**Owner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**Type** <br/> |Required  <br/> |System.Nullable  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Mapping** <br/> |Optional  <br/> |System.String  <br/> ||
|**SourceId** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchLanguageResourcePhrase](get-spenterprisesearchlanguageresourcephrase.md)
  
[Remove-SPEnterpriseSearchLanguageResourcePhrase](remove-spenterprisesearchlanguageresourcephrase.md)

