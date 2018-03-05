---
title: "Set-SPEnterpriseSearchQuerySpellingCorrection"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c0d069e-d7a8-4341-901a-922188a17705

description: "Sets the operation status of the Query Spelling Corrections (QSC) component."
---

# Set-SPEnterpriseSearchQuerySpellingCorrection

Sets the operation status of the Query Spelling Corrections (QSC) component.
  
```
Set-SPEnterpriseSearchQuerySpellingCorrection -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-ContentAlignmentEnabled <$true | $false>] [-DiacriticsInSuggestionsEnabled <$true | $false>] [-Identity <QuerySpellingCorrectionPipeBind>] [-MaxDictionarySize <Int32>] [-MaxProcessingTime <TimeSpan>] [-SecurityTrimmingEnabled <$true | $false>] [-SpellingDictionary <Dynamic | Static>] [-TermFrequencyThreshold <Int32>]

```

## Example

------------------EXAMPLE-----------------
  
```
$searchApp = Get-SPEnterpriseSearchServiceApplication

```

```
Set-SpEnterpriseSEarchQuerySpellingCorrection -SearchApplication $searchApp -SpellingDictionary dynamic
```

This example sets the dictionary named  `dynamic` to be used for query spelling correction for the default search service application. 
  
## Detailed Description

This cmdlet provides access to the configuration options for the QSC component. The two most prominent configuration options are the switch to enable the content-alignment process, and the selection of dictionaries to be used for query spelling correction, that is the set of fixed dictionaries per language or the dynamic dictionary that is being produced by the content alignment process.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search service application that contains the QSC components.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _ContentAlignmentEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |A Boolean value to enable or deactivate the content alignment process.  <br/> |
| _DiacriticsInSuggestionsEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |A switch to enable or disable spelling suggestions that contain diacritics (for example, German umlaut). The default setting is true.  <br/> |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.QuerySpellingCorrectionPipeBind  <br/> |Specifies an object that represents the current status for the query spelling correction.  <br/> |
| _MaxDictionarySize_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximal number of terms in a content-aligned spelling dictionary. In a multi-tenant environment, this number is valid per tenant.  <br/> |
| _MaxProcessingTime_ <br/> |Optional  <br/> |System.TimeSpan  <br/> |Specifies the maximum runtime for compiling a content-aligned spelling dictionary. The default value is 6 hours.  <br/> |
| _SecurityTrimmingEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |A Boolean value to enable or disable the security check for spelling suggestions. If enabled, only spelling suggestions that deliver at least one document for the current user are shown.  <br/> |
| _SpellingDictionary_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.SpellingDictionaryType  <br/> |Specifies the dictionary to be used for query spelling correction. The two available values are **dynamic** and **static**. When value is set to **dynamic**, the query spelling correction uses the content-aligned dictionary. When value is set to **static**, the query spelling correction uses the out of the box static spelling dictionaries.  <br/> |
| _TermFrequencyThreshold_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the minimum number of documents that must contain the most frequently used term in the document collection for the content-alignment process to be executed. In a multi-tenant environment, this number is valid per tenant.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.QuerySpellingCorrectionPipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**ContentAlignmentEnabled** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**DiacriticsInSuggestionsEnabled** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaxDictionarySize** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaxProcessingTime** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**SecurityTrimmingEnabled** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**SpellingDictionary** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**TermFrequencyThreshold** <br/> |Optional  <br/> |System.Nullable  <br/> ||
   

