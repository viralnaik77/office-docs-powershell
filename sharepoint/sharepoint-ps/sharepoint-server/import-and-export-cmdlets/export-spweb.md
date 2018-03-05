---
title: "Export-SPWeb"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 7/20/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cd85bf19-6f24-4f13-bd9c-37bbf279ea2b

description: "Exports a site, list, or library."
---

# Export-SPWeb

Exports a site, list, or library.
  
```
Export-SPWeb -Identity <SPWebPipeBind> -Path <String> [-AppLogFilePath <String>] [-AssignmentCollection <SPAssignmentCollection>] [-CompressionSize <Int32>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-HaltOnError <SwitchParameter>] [-HaltOnWarning <SwitchParameter>] [-IncludeAlerts <SwitchParameter>] [-IncludeUserSecurity <SwitchParameter>] [-IncludeVersions <LastMajor | CurrentVersion | LastMajorAndMinor | All>] [-ItemUrl <String>] [-NoFileCompression <SwitchParameter>] [-NoLogFile <SwitchParameter>] [-UseSqlSnapshot <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------------------EXAMPLE 1-----------------------.
  
```
Export-SPWeb http://site -Path "site export.cmp"
```

This example exports the site at http://site/ to a file called  `site export.cmp` in the current directory. 
  
--------------------EXAMPLE 2-----------------------.
  
```
Export-SPWeb -Identity "http://content.site.local" -ItemUrl "/Lists/listName" -Path "c:\list-export.cmp"
```

This example exports a list that exists in the root site collection.
  
--------------------EXAMPLE 3-----------------------.
  
```
Export-SPWeb -Identity "http://content.site.local/sites/site-collectionName/" -ItemUrl "Lists/listName" -Path "c:\list-export.cmp"
```

This example exports a list that does not exist in the root site collection.
  
> [!NOTE]
> The differences are in the trailing slash. If exporting from the root site collection, you need to provide a forward slash on the **ItemUrl** parameter. If you are exporting from a site collection that is not root, then you need to ensure that the **Identity** parameter contains a forward slash as the last character of the Url. 
  
## Detailed Description

The **Export-SPWeb** cmdlet exports a site, list, or library. The capability to export from a library is a new feature in SharePoint Server 2016. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the URL or GUID of the Web to be exported.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint site (for example, MySPSite1); or an instance of a valid **SPWeb** object.  <br/> |
| _Path_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the export file.  <br/> If the **NoFileCompression** parameter is used, a directory must be specified; otherwise, any file format is valid.  <br/> |
| _AppLogFilePath_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the application log file path  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CompressionSize_ <br/> |Optional  <br/> |System.Int32  <br/> |Sets the maximum file size for the compressed export files. If the total size of the exported package is greater than this size, the exported package will be split into multiple files.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Force_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forcefully overwrites the export package if it already exists.  <br/> The type must be either of the following values:  <br/> - **True** <br/> - **False** <br/> The default value is **False**.  <br/> |
| _HaltOnError_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Stops the export process when an error occurs.  <br/> |
| _HaltOnWarning_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Stops the export process when a warning occurs.  <br/> |
| _IncludeAlerts_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Indicates if alerts are turned on.  <br/> |
| _IncludeUserSecurity_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Preserves the user security settings except for SPLists that have broken inheritance and item level permissions set.  <br/> |
| _IncludeVersions_ <br/> |Optional  <br/> |Microsoft.SharePoint.Deployment.SPIncludeVersions  <br/> |Indicates the type of file and list item version history to be included in the export operation. If the **IncludeVersions** parameter is absent, the Export-SPWeb cmdlet by default uses a value of **1**.  <br/> The type must be any one of the following versions:  <br/> -Last major version for files and list items (default)  <br/> -The current version, either the last major version or the last minor version  <br/> -Last major and last minor version for files and list items  <br/> -All versions for files and list items  <br/> |
| _ItemUrl_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the URL of the Web application, GUID, or object to be exported.  <br/> The type must be a valid URL; for example, http://server_name.  <br/> |
| _NoFileCompression_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Either enables or disables file compression in the export package. The export package is stored in the folder specified by the **Path** parameter or **Identity** parameter. We recommend that you use this parameter for performance reasons. If compression is enabled, the export process can increase by approximately 30 percent.  <br/> |
| _NoLogFile_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Suppresses the generation of an export log file. If this parameter is not specified, the **Export-SPWeb** cmdlet will generate an export log file in the same location as the export package. The log file uses Unified Logging Service (ULS).  <br/> It is recommended to use this parameter. However, for performance reasons, you might not want to generate a log file.  <br/> |
| _UseSqlSnapshot_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies a SQL Database Snapshot will be created when the export process begins, and all exported data will be retrieved directly from the database snapshot. This snapshot will be automatically deleted when export completes.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Get-SPWeb](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/get-spweb.md)
  
[New-SPWeb](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/new-spweb.md)
  
[Set-SPWeb](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/set-spweb.md)
  
[Import-SPWeb](import-spweb.md)
  
[Remove-SPWeb](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/remove-spweb.md)

