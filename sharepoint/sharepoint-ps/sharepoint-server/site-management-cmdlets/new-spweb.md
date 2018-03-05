---
title: "New-SPWeb"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1ea28725-5b75-49f9-b69c-5ff0edf31459

description: "Creates a new site in an existing site collection."
---

# New-SPWeb

Creates a new site in an existing site collection.
  
```
New-SPWeb [-Url] <String> [-AddToQuickLaunch <SwitchParameter>] [-AddToTopNav <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Description <String>] [-Language <UInt32>] [-Name <String>] [-Template <SPWebTemplatePipeBind>] [-UniquePermissions <SwitchParameter>] [-UseParentTopNav <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **New-SPWeb** cmdlet creates a new site in the existing site collection specified by the **Url** parameter. You can create a site with a specific default language by specifying the **Language** parameter. If no language is specified, the site is created with the same language that was specified when the product was installed. You can create a site from a specific template by specifying the **Template** parameter. If no template is specified, the site is created and the template can be provided later or by the first user to log on. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Url** <br/> |Required  <br/> |System.String  <br/> |Specifies the URL where the new site is to be created. The URL must be inside an existing site collection. The URL must be a valid URL, in the form http://server_name/site1.  <br/> |
|**Language** <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the language template identifier for the new site. If no language is specified, the site is created with the same language that was specified when the product was installed.  <br/> The type must be a valid language identifier (LCID).  <br/> |
|**Template** <br/> |Optional  <br/> |SPWebTemplatePipeBind  <br/> |Specifies the Web template for the new site. The template must already exist. If no template is specified, no template is applied and a template can be selected later.  <br/> |
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the title of the new site. If no title is specified, the default title is applied. The default title is configured for each template.  <br/> |
|**Description** <br/> |Optional  <br/> |System.String  <br/> |Describes the new site. If no description is specified, the entry is left blank.  <br/> |
|**AddToQuickLaunch** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Adds this site to the Quick Launch.  <br/> |
|**UniquePermissions** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that this site is to be created with unique permissions.  <br/> |
|**AddToTopNav** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Adds this site to the top-level navigation bar.  <br/> |
|**UseParentTopNav** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the same top-level navigation bar as the parent site is to be used for this site.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Url** <br/> |Required  <br/> |System.String  <br/> ||
|**AddToQuickLaunch** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AddToTopNav** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Description** <br/> |Optional  <br/> |System.String  <br/> ||
|**Language** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**Template** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebTemplatePipeBind  <br/> ||
|**UniquePermissions** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**UseParentTopNav** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Input Types

none
  
## Example

------------------EXAMPLE-----------------------
  
```
New-SPWeb http://somesite/subweb1 -Template "STS#0"
```

This example creates a new subsite by using the Team Site template at the provided URL ( `http://somesite/subweb1`). The Team Site template is a value referenced as the variable  `STS#0` for the  `Template` parameter. 
  
## See also

#### 

[Get-SPWeb](get-spweb.md)
  
[Set-SPWeb](set-spweb.md)
  
[Remove-SPWeb](remove-spweb.md)
  
[Import-SPWeb](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/import-and-export-cmdlets/import-spweb.md)

