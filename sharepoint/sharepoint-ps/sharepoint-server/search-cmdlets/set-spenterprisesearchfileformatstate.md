---
title: "Set-SPEnterpriseSearchFileFormatState"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e02ccce0-3c16-4d25-bf6d-1cabeb67907f

description: "Enables or disables parsing of a specified file format."
---

# Set-SPEnterpriseSearchFileFormatState

Enables or disables parsing of a specified file format.
  
```
Set-SPEnterpriseSearchFileFormatState -Enable <$true | $false> -Identity <DocumentParserFileFormatStatePipeBind> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-UseIFilter <$true | $false>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------EXAMPLE 1--------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
Set-SPEnterpriseSearchFileFormatState -SearchApplication $ssa PDF $FALSE
```

This example uses the **Set-SPEnterpriseSearchFileFormatState** cmdlet to disable the format handler for the file format "PDF." 
  
--------EXAMPLE 2--------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
Set-SPEnterpriseSearchFileFormatState -SearchApplication $ssa PDF $TRUE $TRUE

```

This example uses the **Set-SPEnterpriseSearchFileFormatState** cmdlet to set the content processing component to parse the file format "PDF" with a third-party iFilter. Ensure that you install the third-party iFilter. 
  
## Detailed Description

The **Set-SPEnterpriseSearchFileFormatState** cmdlet enables or disables the content processing component from parsing a specified file format. See [Default crawled file name extensions and parsed file types in SharePoint Server 2013](http://technet.microsoft.com/library/19d553a7-7001-4b07-a03d-616b865b05ae.aspx) to see which file formats that SharePoint Server 2016 parses by default. 
  
The **Set-SPEnterpriseSearchFileFormatState** cmdlet can also set the content processing component to use a third-party iFilter to parse the specified file format. You can only use this cmdlet for file formats that the content processing component parses with a built-in format handler or a built-in iFilter. Use the **Get-SPEnterpriseSearchFileFormat** cmdlet to verify that the content processing component uses a built-in format handler or built-in iFilter for the specified file format 
  
To enable parsing of the specified file format, set  _Enabled_ to "$TRUE". To disable parsing of the specified file format, set  _Enabled_ to "$FALSE". 
  
The content processing component uses the built-in format handler or built-in iFilter to parse the specified file format when  _UseIFilter_ is "$FALSE". The default value for  _UseIFilter_ is "$FALSE". To set the content processing component to parse the specified file format with a third-party iFilter, set UseIFilter to "$TRUE". The content processing component uses the most recently installed third-party iFilter to parse the specified file format. If you don't install the third-party iFilter, the content processing component can't parse the file format. Failure to parse a file format is logged in the crawl log. 
  
> [!NOTE]
> A file format can support more than one file name extension, see [Default crawled file name extensions and parsed file types in SharePoint Server 2013](http://technet.microsoft.com/library/19d553a7-7001-4b07-a03d-616b865b05ae.aspx) for an overview. The **Set-SPEnterpriseSearchFileFormatState** cmdlet enables or disables parsing of all file name extensions the file format supports. 
  
Your change is effective after you restart the SharePoint Server 2016 Search Host Controller process of each server that hosts a content processing component in the Search service application.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Enable_ <br/> |Required  <br/> |System.Boolean  <br/> |Specifies the activation state of the file format. The activation state can be $FALSE (disabled) or $TRUE (enabled).  <br/> |
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.DocumentParserFileFormatStatePipeBind  <br/> |Specifies the identification of the file format to be disabled or enabled.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the name of the search application that contains the file format. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _UseIFilter_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies use of a third-party iFilter when parsing the file format. UseIFilter can be $FALSE (built-in format handler is used) or $TRUE (third-party iFilter is used). $FALSE is the default value.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.DocumentParserFileFormatStatePipeBind  <br/> ||
|**Enable** <br/> |Required  <br/> |System.Boolean  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchFileFormat](new-spenterprisesearchfileformat.md)
  
[Get-SPEnterpriseSearchFileFormat](get-spenterprisesearchfileformat.md)
  
[Remove-SPEnterpriseSearchFileFormat](remove-spenterprisesearchfileformat.md)

