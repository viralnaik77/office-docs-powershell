---
title: "Import-SPEnterpriseSearchCustomExtractionDictionary"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d6287c5-d439-4233-9ddb-9ee19f2d2112

description: "Imports a custom entity extraction dictionary."
---

# Import-SPEnterpriseSearchCustomExtractionDictionary

Imports a custom entity extraction dictionary.
  
```
Import-SPEnterpriseSearchCustomExtractionDictionary -DictionaryName <String> -FileName <String> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE-----------------
  
```
$searchApp = Get-SPEnterpriseSearchServiceApplication

```

```
Import-SPEnterpriseSearchCustomExtractionDictionary -SearchApplication $searchApp -Filename \\host\share\entity_extraction.csv -DictionaryName Microsoft.UserDictionaries.EntityExtraction.Custom.Word.1
```

This example imports the custom entity extraction dictionary that is located at  `\\host\share` to the default search service application. The entries of this dictionary will be matched in a case-insensitive way against the terms in the documents being indexed. 
  
## Detailed Description

This cmdlet imports a custom entity extraction dictionary from a .csv file. In order to activate custom entity extraction you must also configure entity extraction in the search schema.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _DictionaryName_ <br/> |Required  <br/> |System.String  <br/> | Specifies the name of the target dictionary. The name must be one of the following 12 predefined dictionaries. The name signifies the "case sensitivity" and "token matching" behavior.  <br/>  Microsoft.UserDictionaries.EntityExtraction.Custom.Word.1  <br/>  Microsoft.UserDictionaries.EntityExtraction.Custom.Word.2  <br/>  Microsoft.UserDictionaries.EntityExtraction.Custom.Word.3  <br/>  Microsoft.UserDictionaries.EntityExtraction.Custom.Word.4  <br/>  Microsoft.UserDictionaries.EntityExtraction.Custom.Word.5  <br/>  Microsoft.UserDictionaries.EntityExtraction.Custom.ExactWord.1  <br/>  Microsoft.UserDictionaries.EntityExtraction.Custom.WordPart.1  <br/>  Microsoft.UserDictionaries.EntityExtraction.Custom.WordPart.2  <br/>  Microsoft.UserDictionaries.EntityExtraction.Custom.WordPart.3  <br/>  Microsoft.UserDictionaries.EntityExtraction.Custom.WordPart.4  <br/>  Microsoft.UserDictionaries.EntityExtraction.Custom.WordPart.5  <br/>  Microsoft.UserDictionaries.EntityExtraction.Custom.ExactWordPart.1  <br/> |
| _FileName_ <br/> |Required  <br/> |System.String  <br/> |Specifies the full UNC (Universal Naming Convention) path of the .csv file to be imported.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search service application to which the custom entity extraction dictionary should be imported.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**DictionaryName** <br/> |Required  <br/> |System.String  <br/> ||
|**FileName** <br/> |Required  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Create and deploy custom entity extractors in SharePoint 2013](http://technet.microsoft.com/library/055e27eb-3e02-4470-a037-5896bab44736.aspx)

