---
title: "Uninstall-SPWebPartPack"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8103c7d5-3b5b-4281-b9b6-e5ad93d3e2ef

description: "Uninstalls the specified Web Part package."
---

# Uninstall-SPWebPartPack

Uninstalls the specified Web Part package.
  
```
Uninstall-SPWebPartPack [-Identity] <String> [-AssignmentCollection <SPAssignmentCollection>] [-CompatibilityLevel <String>] [-Confirm [<SwitchParameter>]] [-Language <UInt32>] [-WebApplication <SPWebApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]

```

## Detailed Description

The **Uninstall-SPWebPartPack** cmdlet uninstalls the Web Part package specified by the **Identity** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |System.String  <br/> |Specifies the Web Part package in the farm's configuration database.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CompatibilityLevel** <br/> |Optional  <br/> |System.String  <br/> |Specifies the version of templates to use when creating a new **SPSite** object. This value sets the initial CompatibilityLevel value for the site collection. When this parameter is not specified, the CompatibilityLevel will default to the highest possible version for the web application depending on the SiteCreationMode setting.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Language** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the language ID of the Web Part package to delete. If no language is specified, the Web Part package is uninstalled for all languages.  <br/> The type must be a valid language identifier, in the form 1033.  <br/> |
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the Web application from which to uninstall the Web Part package. If no Web application is specified, the Web Part package is uninstalled from all Web applications.  <br/> The type must be a valid name, in the form WebApplication-1212, or a URL, in the form http://server_name/WebApplication-1212.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CompatibilityLevel** <br/> |Optional  <br/> |System.String  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Language** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Return Types

None
  
## Errors

|**Error**|**Description**|
|:-----|:-----|
|||
   
## Exceptions

|**Exceptions**|**Description**|
|:-----|:-----|
|||
   
## Example

------------------EXAMPLE1------------------
  
```
Uninstall-SPWebPartPack  "mypart.wpp" -WebApplication http://portal
```

This example uninstalls  `mypart.wpp` to from the Web application  `http://portal`.
  
------------------EXAMPLE2------------------
  
```
Get-SPWebPartPack -WebApplication http://portal | Uninstall-SPWebPartPack
```

This example uninstalls all Web part packages from the Web application  `http://portal`.
  
## See also

#### 

[Get-SPWebPartPack](get-spwebpartpack.md)
  
[Install-SPWebPartPack](install-spwebpartpack.md)

