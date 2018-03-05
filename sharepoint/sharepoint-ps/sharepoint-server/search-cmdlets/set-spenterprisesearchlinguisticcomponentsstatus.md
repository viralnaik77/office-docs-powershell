---
title: "Set-SPEnterpriseSearchLinguisticComponentsStatus"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3abe030d-3b13-4b19-bbd7-4db87ca3c527

description: "Sets the operation status of the linguistic query and document processing components."
---

# Set-SPEnterpriseSearchLinguisticComponentsStatus

Sets the operation status of the linguistic query and document processing components.
  
```
Set-SPEnterpriseSearchLinguisticComponentsStatus -SearchApplication <SearchServiceApplicationPipeBind> [-AllEnabled <$true | $false>] [-AssignmentCollection <SPAssignmentCollection>] [-EntityExtractionEnabled <$true | $false>] [-Identity <LinguisticComponentsStatusPipeBind>] [-QuerySpellingEnabled <$true | $false>] [-StemmingEnabled <$true | $false>] [-ThesaurusEnabled <$true | $false>]

```

## Example

------------------EXAMPLE 1-----------------
  
```
$searchApp = Get-SPEnterpriseSearchServiceApplicationSet-SpEnterpriseSearchLinguisticComponentsStatus -SearchApplication $searchApp -StemmingEnabled $false 
```

This example shows how to disable stemming during query processing by setting the parameter  `StemmingEnabled` to false. 
  
------------------EXAMPLE 2-----------------
  
```
$searchApp = Get-SPEnterpriseSearchServiceApplicationSet-SpEnterpriseSearchLinguisticComponentsStatus -SearchApplication $searchApp -AllEnabled $false 
```

This example shows how to disable all linguistic query and document processing functionalities. 
  
## Detailed Description

This cmdlet sets the operational status of the linguistic query and document processing components. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search service application that contains the linguistic processing components.  <br/> |
| _AllEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |A Boolean value to enable or deactivate all linguistic functionalities.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _EntityExtractionEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |A Boolean value to enable or deactivate the  *company*  extractor and all custom extractors during document processing.  <br/> |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.LinguisticComponentsStatusPipeBind  <br/> |An object that represents the current status of the linguistic components.  <br/> |
| _QuerySpellingEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |A Boolean value to enable or deactivate query spelling correction.  <br/> |
| _StemmingEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |A Boolean value to enable or deactivate expansive stemming during query processing.  <br/> |
| _ThesaurusEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |A Boolean value to enable or deactivate thesaurus lookup during query processing.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.LinguisticComponentsStatusPipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AllEnabled** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**EntityExtractionEnabled** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**QuerySpellingEnabled** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**StemmingEnabled** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**ThesaurusEnabled** <br/> |Optional  <br/> |System.Nullable  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchLinguisticComponentsStatus](get-spenterprisesearchlinguisticcomponentsstatus.md)

