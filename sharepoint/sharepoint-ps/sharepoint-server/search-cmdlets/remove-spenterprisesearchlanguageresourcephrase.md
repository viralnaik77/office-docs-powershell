---
title: "Remove-SPEnterpriseSearchLanguageResourcePhrase"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 135519df-dc6e-446d-9a61-0cd8fee4ca1a

description: "Deletes a language resource phrase from a shared search application."
---

# Remove-SPEnterpriseSearchLanguageResourcePhrase

Deletes a language resource phrase from a shared search application.
  
```
Remove-SPEnterpriseSearchLanguageResourcePhrase -Identity <LanguageResourcePhrasePipeBind> -Owner <SearchObjectOwner> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Language <String>] [-Mapping <String>] [-SearchApplication <SearchServiceApplicationPipeBind>] [-SourceId <Guid>] [-Type <Undefined | QuerySuggestionBlockList | QuerySuggestionAlwaysSuggest | SpellingSuggestionBlockList | SummaryNoiseList | Nickname | LastNameMap | FirstNameMap | SpellingSuggestionAlwaysSuggest | CharacterMap | QuerySuggestionSubstitution>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication "SearchApp1"$obsoletephrase = Get-SPEnterpriseSearchLanguageResourcePhrase -SearchApplication $searchapp -Language en-us -Type QuerySuggestionBlockList -Identity secret$obsoletephrase | Remove-SPEnterpriseSearchLanguageResourcePhrase -SearchApplication $searchapp -Type QuerySuggestionBlockList -Language en-us
```

This example removes a language resource item on the  `QuerySuggestionBlockList` for the  `en-us` language. 
  
## Detailed Description

The **Remove-SPEnterpriseSearchLanguageResourcePhrase** cmdlet deletes one or more language resource phrases from the collection of language resource phrases in a shared search application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.LanguageResourcePhrasePipeBind  <br/> |The language resource phrase to delete.  <br/> The type must be a string; a valid name of a language resource phrase (for example, LanguageResourcePhrase1); or an instance of a valid **LanguageResourcePhrase** object.  <br/> |
| _Owner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the search object owner that defines the scope at which the corresponding **LanguageResourcePhrase** is created.  <br/> The owner must be one of the following valid levels:  <br/> - Search Service Application  <br/> - Site Subscription  <br/> - Site Collection  <br/> - Site  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Language_ <br/> |Optional  <br/> |System.String  <br/> |Deletes phrases of the specified language only.  <br/> The type must be a valid name of a language; for example, en_us.  <br/> |
| _Mapping_ <br/> |Optional  <br/> |System.String  <br/> |Allows a term or phrase to be mapped to another term or phrase. For example, the nickname "John" could be mapped to "Jonathan".  <br/> This parameter only applies to nicknames and substitutions.  <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the language resources.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _SourceId_ <br/> |Optional  <br/> |System.Guid  <br/> |Identifies the search result source for which the **LanguageResourcePhrase** applies to.  <br/> |
| _Type_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.LanguageResourceType  <br/> |Constrains to delete phrases of specified type.  <br/> The type must be one of the following valid types of phrases:  <br/> - QuerySuggestionBlockList  <br/> - QuerySuggestionAlwaysSuggest  <br/> - Nickname  <br/> - QuerySuggestionSubstitution  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.LanguageResourcePhrasePipeBind  <br/> ||
|**Owner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Language** <br/> |Optional  <br/> |System.String  <br/> ||
|**Mapping** <br/> |Optional  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**SourceId** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**Type** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchLanguageResourcePhrase](get-spenterprisesearchlanguageresourcephrase.md)
  
[New-SPEnterpriseSearchLanguageResourcePhrase](new-spenterprisesearchlanguageresourcephrase.md)

