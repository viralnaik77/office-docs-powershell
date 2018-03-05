---
title: "New-SPEnterpriseSearchCrawlCustomConnector"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9cfc9653-9bee-4c3a-8739-9bc81aa3e699

description: "Registers a protocol for custom crawling."
---

# New-SPEnterpriseSearchCrawlCustomConnector

Registers a protocol for custom crawling.
  
```
New-SPEnterpriseSearchCrawlCustomConnector -ModelFilePath <String> -Protocol <String> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Name <String>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$searchApp = Get-SPEnterpriseSearchServiceApplication mySearchServiceAppNew-SPEnterpriseSearchCrawlCustomConnector -SearchApplication $searchApp -ModelFilePath \\models\myFileTypeModel.mft -Protocol "mftml://"
```

This example creates a custom connector for a file type whose model is located at  `\\models\myFileTypeModel.mft` and has the protocol name  `mftml://`.
  
## Detailed Description

The **New-SPEnterpriseSearchCrawlCustomConnector** cmdlet registers, for a search system, the protocol that is used to crawl the custom repository. 
  
If the **Name** parameter is not provided, in the administration application user interface (UI) the name **protocol** identifies the protocol specified. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ModelFilePath_ <br/> |Required  <br/> |System.String  <br/> |Specifies the path to a model file.  <br/> |
| _Protocol_ <br/> |Required  <br/> |System.String  <br/> |Specifies the string version of the protocol; for example, dctm://.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that is associated with the protocol.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the display name of the custom connector that appears on the SharePoint Central Administration Web site.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ModelFilePath** <br/> |Required  <br/> |System.String  <br/> ||
|**Protocol** <br/> |Required  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   

