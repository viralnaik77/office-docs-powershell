---
title: "Restore-SPDeletedSite"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d05cf671-2c54-41f1-96e5-fbb116102e9b

description: "Restores a deleted site collection."
---

# Restore-SPDeletedSite

Restores a deleted site collection.
  
```
Restore-SPDeletedSite [-Identity] <SPDeletedSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-ContentDatabase <SPContentDatabasePipeBind>] [-WebApplication <SPWebApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet was introduced in SharePoint Server 2010 with Service Pack 1 (SP1) and SharePoint Foundation 2010 with Service Pack 1 (SP1).
  
Use the **Restore-SPDeletedSite** cmdlet to restore a previously deleted site collection. 
  
Unlike the [Restore-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/backup-and-recovery-cmdlets/restore-spsite.md) cmdlet that uses the host name and scheme for the **Identity** parameter (that is, http://server_name), the value of the identity parameter for all **SPDeletedSite** cmdlets use a server-relative URL. Typically, the forward slash character (/) begins the relative URL and also denotes the root site. 
  
For additional information about a server-relative URL or understanding general concepts about absolute and relative URLs, see [Server-relative URL Property](https://msdn.microsoft.com/en-us/library/microsoft.sharepoint.spsite.serverrelativeurl.aspx) or [Understanding Absolute and Relative URL Addresses](https://msdn.microsoft.com/en-us/library/bb208688%28office.12%29.aspx).
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPDeletedSitePipeBind  <br/> |Specifies the identity of the deleted site collection to be restored. The identity can be either a valid server-relative URL in the form /sites/site_name; a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an **SPDeletedSite** object  <br/> A site collection must not already exist at the URL location to perform a restore.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**ContentDatabase** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the SQL Server content database where the site collection data will be stored. If no content database is specified, the content database with the greatest unused site collection capacity and whose database status is ready will be used.  <br/> |
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the URL, GUID, or name of the Web application from which to list sites.  <br/> The type must be a valid URL in the form http://server_name; a valid GUID, for example, 12345678-90ab-cdef-1234-567890bcdefgh; or the Web application name, for example, WebApplication1212.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPDeletedSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ContentDatabase** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> ||
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

----------------------EXAMPLE 1---------------------- 
  
```
Restore-SPDeletedSite -Identity 610857cb-8414-4a89-8bf3-ad3628f6c86c
```

This example restores a specific deleted site collection by using the site ID.
  
## See also

#### 

[Get-SPDeletedSite](get-spdeletedsite.md)
  
[Remove-SPDeletedSite](remove-spdeletedsite.md)

