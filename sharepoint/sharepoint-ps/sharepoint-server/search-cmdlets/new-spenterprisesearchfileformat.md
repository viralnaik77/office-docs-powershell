---
title: "New-SPEnterpriseSearchFileFormat"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 31eda9aa-0214-4765-a949-75ad209e4c79

description: "Adds the ability to parse a new file format."
---

# New-SPEnterpriseSearchFileFormat

Adds the ability to parse a new file format.
  
```
New-SPEnterpriseSearchFileFormat -FormatId <String> -FormatName <String> -MimeType <String> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

-------------EXAMPLE-------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
New-SPEnterpriseSearchFileFormat -SearchApplication $ssa sample SampleApp application/SampleApp
```

This example uses the **New-SPEnterpriseSearchFileFormat** cmdlet to enable the content processing component in the Search service application referenced by  `$ssa` to parse files that have the file name extension "sample", the file format "SampleApp", and the mime type "application/SampleApp". 
  
## Detailed Description

The **New-SPEnterpriseSearchFileFormat** cmdlet enables the content processing component to parse files with a specified file format and file name extension. The cmdlet can only enable parsing of the file format and file name extension if the server that hosts the content processing component has a relevant third-party filter-based format handler (iFilter) installed. You can use the **Get-SPEnterpriseSearchFileFormat** cmdlet to verify that an iFilter is installed for a specified file format. 
  
During iFilter installation, the operating system registered the iFilter with one or more file name extensions. Use the **New-SPEnterpriseSearchFileFormat** cmdlet for each registered file name extension that you want to enable the content processing component to parse. Do this on each server that hosts a content processing component in the Search service application. 
  
Your change is effective after you restart the SharePoint Server 2016 Search Host Controller process of each server that hosts a content processing component in the Search service application.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _FormatId_ <br/> |Required  <br/> |System.String  <br/> |Specifies the file name extension of the format to parse.  <br/> |
| _FormatName_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the format to parse. Usually this is the name of the application handling the format.  <br/> |
| _MimeType_ <br/> |Required  <br/> |System.String  <br/> |Specifies the mime type of the format to parse.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application for which to add the new file format. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**FormatId** <br/> |Required  <br/> |System.String  <br/> ||
|**FormatName** <br/> |Required  <br/> |System.String  <br/> ||
|**MimeType** <br/> |Required  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchFileFormat](get-spenterprisesearchfileformat.md)
  
[Remove-SPEnterpriseSearchFileFormat](remove-spenterprisesearchfileformat.md)
#### 

[Set-SPEnterpriseSearchFileFormatState](set-spenterprisesearchfileformatstate.md)

