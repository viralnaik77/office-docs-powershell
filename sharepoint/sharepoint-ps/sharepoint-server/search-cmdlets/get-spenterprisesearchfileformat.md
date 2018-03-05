---
title: "Get-SPEnterpriseSearchFileFormat"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5813415a-a741-4371-9500-fd8e0dfb6977

description: "Retrieves all file formats that the parsing system has format handlers for."
---

# Get-SPEnterpriseSearchFileFormat

Retrieves all file formats that the parsing system has format handlers for.
  
```
Get-SPEnterpriseSearchFileFormat -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <DocumentParserFileFormatPipeBind>]

```

## Example

-------------EXAMPLE 1-------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
Get-SPEnterpriseSearchFileFormat -SearchApplication $ssa
```

This example uses the **Get-SPEnterpriseSearchFileFormat** to retrieve all file formats that the Search service application referenced by  `$ssa` has format handlers for. 
  
-------------EXAMPLE 2-------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
Get-SPEnterpriseSearchFileFormat -SearchApplication $ssa zip

```

This example uses the **Get-SPEnterpriseSearchFileFormat** cmdlet to retrieve information about the file format "zip" in the Search service application referenced by  `$ssa`. The result is as follows:
  
Identity :zip
  
Name :ZIP Archive
  
MimeType :application/zip
  
Extension :.zip
  
BuiltIn :True
  
Enabled :False
  
UseIFilter :False
## Detailed Description

The **Get-SPEnterpriseSearchFileFormat** cmdlet retrieves the following information about the specified file format: 
  
- The file name extension.
    
- The mime type of the file format.
    
- The type of format handler the content processing component by default uses to parse the format. The entry "BuiltIn:True" indicates a built-in format handler. The entry "BuiltIn:False" indicates a third-party filter-based format handler (iFilter). 
    
- The parsing state for the format. The entry "Enabled:True" indicates that parsing is enabled. The entry "Enabled:False" indicates that parsing is disabled.
    
- The use of a third-party iFilter to parse the file format. The entry "UseIFilter:True" indicates that the content processing component is set to use a third-party iFilter when parsing the file format.
    
If you do not specify a format ID, the cmdlet returns the list of information for all the file formats that the content processing component has format handlers for.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the Search application for which to retrieve file format information. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.DocumentParserFileFormatPipeBind  <br/> |Specifies the format ID for which to retrieve file format information.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.DocumentParserFileFormatPipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchFileFormat](new-spenterprisesearchfileformat.md)
  
[Remove-SPEnterpriseSearchFileFormat](remove-spenterprisesearchfileformat.md)
#### 

[Set-SPEnterpriseSearchFileFormatState](set-spenterprisesearchfileformatstate.md)

