---
title: "Remove-SPEnterpriseSearchFileFormat"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6956dda6-e77b-4842-8f51-1bcc510853b6

description: "Disables parsing of a file format."
---

# Remove-SPEnterpriseSearchFileFormat

Disables parsing of a file format.
  
```
Remove-SPEnterpriseSearchFileFormat -Identity <DocumentParserFileFormatPipeBind> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

--------EXAMPLE--------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
Remove-SPEnterpriseSearchFileFormat -SearchApplication $ssa -Identity sample
```

This example uses the **Remove-SPEnterpriseSearchFileFormat** cmdlet to remove the file format with the belonging file name extension "sample" in the Search service application referenced by **$ssa**. 
  
## Detailed Description

The **Remove-SPEnterpriseSearchFileFormat** removes the ability of the content processing component to use a third-party filter-based format handler (iFilter) to parse files with a specified file format and file name extension. You can use the **Get-SPEnterpriseSearchFileFormat** cmdlet to verify that a content processing component uses a third-party iFilter for a specified file format. 
  
During iFilter installation, the operating system registered the iFilter with one or more file name extensions. Use the **Remove-SPEnterpriseSearchFileFormat** cmdlet for each registered file name extension that the content processing component no longer shall parse. Do this on each server that hosts a content processing component in the Search service application. 
  
Your change is effective after you restart the SharePoint Server 2016 Search Host Controller process of each server that hosts a content processing component in the Search service application.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.DocumentParserFileFormatPipeBind  <br/> |Specifies the identification of the format to disable parsing of.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the Search service application that contains the file format.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.DocumentParserFileFormatPipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchFileFormat](new-spenterprisesearchfileformat.md)
  
[Get-SPEnterpriseSearchFileFormat](get-spenterprisesearchfileformat.md)
#### 

[Set-SPEnterpriseSearchFileFormatState](set-spenterprisesearchfileformatstate.md)

