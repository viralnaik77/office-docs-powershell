---
title: "Get-SPEnterpriseSearchQuerySpellingCorrection"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4a00b085-917b-48c2-a2cc-8252410b2a24

description: "Returns the object that exposes the Query Spelling Correction (QSC) configuration."
---

# Get-SPEnterpriseSearchQuerySpellingCorrection

Returns the object that exposes the Query Spelling Correction (QSC) configuration.
  
```
Get-SPEnterpriseSearchQuerySpellingCorrection -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <QuerySpellingCorrectionPipeBind>]

```

## Example

------------------EXAMPLE------------------
  
```
$searchApp = Get-SPEnterpriseSearchServiceApplication
```

```
Get-SPEnterpriseSearchQuerySpellingCorrection -SearchApplication $searchApp
```

Returns the current configuration for the Query Spelling Correction component for the default Search service application.
  
## Detailed Description

This cmdlet returns the object that exposes the QSC configuration parameters.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the Search service application that contains the query spelling correction parameters.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.QuerySpellingCorrectionPipeBind  <br/> |Specifies an object that represents the current status for the query spelling correction.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.QuerySpellingCorrectionPipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   

