---
title: "Import-SPWeb"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/11/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2ecc5b6e-1b23-4367-a966-b7bd3377db3a

description: "Imports a web, list, or library."
---

# Import-SPWeb

Imports a web, list, or library.
  
```
Import-SPWeb [-Identity] <SPWebPipeBind> -Path <String> [-ActivateSolutions <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-HaltOnError <SwitchParameter>] [-HaltOnWarning <SwitchParameter>] [-IncludeUserCustomAction <None | All>] [-IncludeUserSecurity <SwitchParameter>] [-NoFileCompression <SwitchParameter>] [-NoLogFile <SwitchParameter>] [-UpdateVersions <Append | Overwrite | Ignore>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Import-SPWeb** cmdlet imports a web, list, or library. The capability to import from a library is a new feature in SharePoint 2010 Products. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the URL or GUID of the Web to import into.  <br/> The type must be a valid URL, GUID, or object; for example, a valid URL, in the form http://server_name, or a GUID, in the form, 1234-4567-5678a.  <br/> |
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the import file.  <br/> If the **NoFileCompression** parameter is used, a directory must be specified; otherwise, any file format is valid.  <br/> |
|**ActivateSolutions** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether user solutions are activated during import.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forcefully overwrites the import package if it already exists.  <br/> The type must be either of the following values  <br/> - **True** <br/> - **False** <br/> The default value is **False**.  <br/> |
|**HaltOnError** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Stops the import process when an error occurs.  <br/> |
|**HaltOnWarning** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Stops the import process when a warning occurs.  <br/> |
|**IncludeUserCustomAction** <br/> |Optional  <br/> |Microsoft.SharePoint.Deployment.SPIncludeUserCustomAction  <br/> |Specifies whether User Custom Actions are included during import.  <br/> |
|**IncludeUserSecurity** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Preserves the user security settings except for SPLists that have broken inheritance and item level permissions set.  <br/> |
|**NoFileCompression** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Either enables or disables file compression in the import package. The import package is stored in the folder specified by the **Path** parameter or **Identity** parameter. We recommend that you use this parameter for performance reasons. If compression is enabled, the import process can increase by approximately 30 percent.  <br/> |
|**NoLogFile** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Suppresses the generation of an import log file. If this parameter is absent, the **Import-SPWeb** cmdlet will generate an export log file in the same location as the export package. The log file uses Unified Logging Service (ULS).  <br/> We recommend that you use this parameter. However, for performance reasons, you might not want to generate a log file.  <br/> |
|**UpdateVersions** <br/> |Optional  <br/> |Microsoft.SharePoint.Deployment.SPUpdateVersions  <br/> |Indicates how to resolve situations where a file version to be imported to a site already exists in that site. The type must be any one of the following:  <br/> **Add** to add the file as a new version.  <br/> **Overwrite** to overwrite the current file and all of its versions (delete then insert)  <br/> **Ignore** to ignore the file if it exists on the destination. The new file will not be added.  <br/> The default value is **Add**.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**ActivateSolutions** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**HaltOnError** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**HaltOnWarning** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**IncludeUserCustomAction** <br/> |Optional  <br/> |Microsoft.SharePoint.Deployment.SPIncludeUserCustomAction  <br/> ||
|**IncludeUserSecurity** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**NoFileCompression** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**NoLogFile** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**UpdateVersions** <br/> |Optional  <br/> |Microsoft.SharePoint.Deployment.SPUpdateVersions  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------------EXAMPLE---------------------- 
  
```
Import-SPWeb http://site -Path export.cmp -UpdateVersions Overwrite
```

This example imports the contents of export.cmp into a site at  `http://site`, overwriting the versioned content on the site with the contents of the  `export.cmp` file. 
  
## See also

#### 

[Export-SPWeb](export-spweb.md)
  
[Get-SPWeb](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/get-spweb.md)
  
[New-SPWeb](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/new-spweb.md)
  
[Remove-SPWeb](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/remove-spweb.md)
  
[Set-SPWeb](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/set-spweb.md)

