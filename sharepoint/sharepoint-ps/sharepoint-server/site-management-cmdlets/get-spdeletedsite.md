---
title: "Get-SPDeletedSite"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9aecd20e-74de-40dc-95dd-e78cf7c1d338

description: "Gets a list of deleted site collections."
---

# Get-SPDeletedSite

Gets a list of deleted site collections.
  
```
Get-SPDeletedSite [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-ContentDatabase <SPContentDatabasePipeBind>] [-DateTimeFrom <String>] [-DateTimeTo <String>] [-Limit <String>] [-SiteSubscription <SPSiteSubscriptionPipeBind>] [-WebApplication <SPWebApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
This cmdlet was introduced in SharePoint Server 2010 with Service Pack 1 (SP1) and SharePoint Foundation 2010 with Service Pack 1 (SP1).
  
Use the **Get-SPDeletedSite** cmdlet to display a list of deleted site collections by using the **Identity** parameter. If no parameter is specified, then all deleted site collections in the farm are displayed. 
  
Unlike the [Get-SPSite](get-spsite.md) cmdlet that uses the host name and scheme for the Identity parameter (that is, http://server_name), the value of the identity parameter for all **SPDeletedSite** cmdlets use a server-relative URL. Typically, the forward slash character (/) begins the relative URL and also denotes the root site. 
  
For additional information about a server-relative URL or understanding general concepts about absolute and relative URLs, see [Server-relative URL Property](https://msdn.microsoft.com/en-us/library/microsoft.sharepoint.spsite.serverrelativeurl.aspx) or [Understanding Absolute and Relative URL Addresses](https://msdn.microsoft.com/en-us/library/bb208688%28office.12%29.aspx).
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPDeletedSitePipeBind  <br/> |Specifies the URL or GUID of the site collection to get.  <br/> The identity can be either a valid server-relative URL in the form /sites/site_name or a valid GUID, for example, 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**ContentDatabase** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the GUID of the content database from which to list site collections.  <br/> The type must be a valid database name in the form SPContentDB01 or a valid GUID, for example, 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
|**DateTimeFrom** <br/> |Optional  <br/> |System.String  <br/> |The type must be a valid DateTime format that is culture-specific to the administrative language, such as 2/16/2007 12:15:12 for English-US.  <br/> |
|**DateTimeTo** <br/> |Optional  <br/> |System.String  <br/> |The type must be a valid DateTime format that is culture-specific to the administrative language, such as 2/16/2007 12:15:12 for English-US.  <br/> |
|**Limit** <br/> |Optional  <br/> |System.String  <br/> |Limits the maximum number of site collections to return. The default value is 1000.  <br/> The type must be a valid non-negative number. Specify ALL to return all site collections for the given scope.  <br/> |
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the site subscription from which to get site collections.  <br/> The type must be a valid URL in the form http://server_name or a valid GUID, for example, 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the URL, GUID, or name of the Web application from which to list sites.  <br/> The type must be a valid URL in the form http://server_name; a valid GUID, for example, 12345678-90ab-cdef-1234-567890bcdefgh; or the Web application name, for example, WebApplication1212.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPDeletedSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ContentDatabase** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> ||
|**DateTimeFrom** <br/> |Optional  <br/> |System.String  <br/> ||
|**DateTimeTo** <br/> |Optional  <br/> |System.String  <br/> ||
|**Limit** <br/> |Optional  <br/> |System.String  <br/> ||
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1---------------------
  
```
Get-SPDeletedSite -Identity 610857cb-8414-4a89-8bf3-ad3628f6c86c
```

This example gets a specific deleted site collection by using a site ID.
  
------------------EXAMPLE 2---------------------
  
```
Get-SPDeletedSite "/" 
```

This example gets a deleted site collection from the root site.
  
------------------EXAMPLE 3---------------------
  
```
Get-SPDeletedSite '/Site/cat*'
```

This example matches a deleted site collection that contains any combination with the string "cat". The asterisk (\*) wildcard character requests a match for multiple characters.
  
## See also

#### 

[Remove-SPDeletedSite](remove-spdeletedsite.md)
  
[Restore-SPDeletedSite](restore-spdeletedsite.md)

