---
title: "Get-SPWeb"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9bf9284f-e3b9-439d-8a5f-74020e1eccaf

description: "Returns all subsites that match the given criteria."
---

# Get-SPWeb

Returns all subsites that match the given criteria.
  
```
Get-SPWeb [[-Identity] <SPWebPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Filter <ScriptBlock>] [-Limit <String>] [-Regex <SwitchParameter>] [-Site <SPSitePipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Get-SPWeb** cmdlet returns all subsites that match the scope given by the **Identity** parameter. All subsites that meet the criteria are returned. 
  
The **Identity** can be either the full URL or a relative path. If you specify a relative path, you must also specify the **Site** parameter to identify the site collection from which to return the subsite. 
  
The **Identity** parameter also supports providing a partial URL that ends in a wildcard character (*). All subsites that match this partial URL for the specified scope are returned. Additionally, if the **Regex** parameter is provided, the **Identity** parameter is treated as a regular expression and any subweb with a URL provided in the given scope that matches the expression is returned. 
  
The **Filter** parameter is a server-side filter for certain subsite properties that are stored in the content database; without the **Filter** parameter, filtering on these properties is a slow process. These subsite properties are **Template** and **Title**. The **Filter** parameter is a script block that uses the same syntax as a Where-Object statement, but is run server-side for faster results. 
  
It is important to note that every site collection returned by the **Get-SPWeb** cmdlet is automatically disposed of at the end of the pipeline. To store the results of **Get-SPWeb** in a local variable, the **Start-SPAssignment** and **Stop-SPAssignment** cmdlets must be used to avoid memory leaks. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the name or full or partial URL of the subsite. If you use a relative path, you must specify the **Site** parameter.  <br/> A valid URL in the form http://server_name or a relative path in the form of /SubSites/MySubSite.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Filter** <br/> |Optional  <br/> |System.Management.Automation.ScriptBlock  <br/> |Specifies the server-side filter to use for the specified scope.  <br/> The type must be a valid filter in the form {filterName \<operator\> "filterValue"}.  <br/> |
|**Limit** <br/> |Optional  <br/> |System.String  <br/> |Limits the maximum number of subsites to return. The default value is **200**. To return all sites, enter ALL <br/> The type must be a valid number greater than 0 or ALL.  <br/> |
|**Regex** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies the URL that is provided by the **Identity** parameter is treated as a regular expression.  <br/> |
|**Site** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the URL or GUID of the site collection from which to list subsites.  <br/> The type must be a valid URL, in the form of http://server_name; a GUID, in the form 1234-5678-9807, or an **SPSite** object.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Filter** <br/> |Optional  <br/> |System.Management.Automation.ScriptBlock  <br/> ||
|**Limit** <br/> |Optional  <br/> |System.String  <br/> ||
|**Regex** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Site** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------------EXAMPLE 1----------------------
  
```
Get-SPWeb -site http://sitename/sites/site1
```

This example returns all the subwebs in a given site collection.
  
--------------------EXAMPLE 2----------------------
  
```
Get-SPWeb -Site http://sitename/sites/site1  -filter {$_.Template -eq "STS#0"}
```

This example displays all subsites that use the  `"STS#0"` template. 
  
--------------------EXAMPLE 3----------------------
  
```
Start-SPAssignment -Global
```

```
$w = Get-SPWeb http://sitename
```

```
$w.set_SiteLogoUrl("http://PathToImage/test.jpg")
```

```
$w.Update()
```

```
Stop-SPAssignment -Global
```

This example demonstrates how to save a subsite as a variable and to call object model methods on the **SPAssignment** object. 
  
## See also

#### 

[New-SPWeb](new-spweb.md)
  
[Set-SPWeb](set-spweb.md)
  
[Remove-SPWeb](remove-spweb.md)
  
[Import-SPWeb](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/import-and-export-cmdlets/import-spweb.md)

