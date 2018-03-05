---
title: "Set-SPWeb"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b21444f-7f4c-4155-8f0d-952b585e4524

description: "Configures the specified subsite."
---

# Set-SPWeb

Configures the specified subsite.
  
```
Set-SPWeb [-Identity] <SPWebPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Description <String>] [-RelativeUrl <String>] [-Template <SPWebTemplatePipeBind>] [-Theme <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPWeb** cmdlet configures the subsite specified by the **Identity** parameter. Settings for any parameters that are not provided are not changed. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |The URL of the Web or **SPWeb** object that represents the Web.  <br/> The type must be a valid URL, in the form http://server_name, or an **SPWeb** object.  <br/> |
|**Name** <br/> |Optional  <br/> |String  <br/> |Specifies the new name of the Web.  <br/> |
|**Description** <br/> |Optional  <br/> |System.String  <br/> |Specifies the new description of the Web.  <br/> |
|**RelativeUrl** <br/> |Optional  <br/> |System.String  <br/> |Specifies the new relative URL for the Web. This is the URL path after the site collection URL.  <br/> |
|**Theme** <br/> |Optional  <br/> |System.String  <br/> |Specifies the new theme to apply to the Web.  <br/> |
|**Template** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebTemplatePipeBind  <br/> |Specifies the new template to apply to the Web. This cannot be done if the template is already applied.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Description** <br/> |Optional  <br/> |System.String  <br/> ||
|**RelativeUrl** <br/> |Optional  <br/> |System.String  <br/> ||
|**Template** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebTemplatePipeBind  <br/> ||
|**Theme** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Return Types

one
  
## Example

------------------EXAMPLE-----------------------
  
```
Get-SPWeb http://sitename/subweb | Set-SPWeb -Title "My Site Title"
```

This example sets the title of an existing subsite.
  
## See also

#### 

[Get-SPWeb](get-spweb.md)
  
[New-SPWeb](new-spweb.md)
  
[Remove-SPWeb](remove-spweb.md)
  
[Export-SPWeb](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/import-and-export-cmdlets/export-spweb.md)
  
[Import-SPWeb](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/import-and-export-cmdlets/import-spweb.md)

