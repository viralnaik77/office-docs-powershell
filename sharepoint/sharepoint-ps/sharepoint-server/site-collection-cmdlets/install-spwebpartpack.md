---
title: "Install-SPWebPartPack"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4245f30-c369-4b91-b4bd-1048a2abd384

description: "Installs the specified Web Part package to the specified location."
---

# Install-SPWebPartPack

Installs the specified Web Part package to the specified location.
  
```
Install-SPWebPartPack [-LiteralPath] <String> [-AssignmentCollection <SPAssignmentCollection>] [-CompatibilityLevel <String>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-GlobalInstall <SwitchParameter>] [-Language <UInt32>] [-WebApplication <SPWebApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]

```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Install-SPWebPartPack** cmdlet installs the Web Part package, at the **LiteralPath** parameter location, in the local farm. The Web Part package can be installed in a specific Web application by using the **WebApplication** parameter. If a Web application is not specified, the Web Part package is installed in all Web applications. 
  
Use the **Language** parameter to specify a package language. 
  
Use the **GlobalInstall** parameter to install the package to the global assembly cache (GAC). Assemblies in the GAC are granted FullTrust permission, which gives this package full access to all system-wide resources. 
  
Use the **Force** parameter to install the package to overwrite any existing Web Part package with the same name or installed in the same location. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**LiteralPath** <br/> |Required  <br/> |System.String  <br/> |Specifies the exact path to the Web Part package.  <br/> |
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the Web Part package to install.  <br/> |
|**AddToLatestVersion** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether to install the solution to the latest version directories or to use only the current version that is tracked in the cab file. The default value is to not add to the latest version directories.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CompatibilityLevel** <br/> |Optional  <br/> |System.String  <br/> |Specifies the version of templates to use when creating a new **SPSite** object. This value sets the initial CompatibilityLevel value for the site collection. When this parameter is not specified, the CompatibilityLevel will default to the highest possible version for the web application depending on the SiteCreationMode setting.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Overwrites any existing Web Part package with the same name or installed in the same location.  <br/> |
|**GlobalInstall** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Installs the Web Part package in the global assembly cache (GAC) rather than in the /bin directory of each Web application. This installation makes the Web Part globally accessible on the servers.  <br/> |
|**Language** <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the language ID for the Web Part package.  <br/> |
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the Web application on which to install the Web Part pack. If no Web application is specified, the Web Part pack is installed on all Web applications.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**LiteralPath** <br/> |Required  <br/> |System.String  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CompatibilityLevel** <br/> |Optional  <br/> |System.String  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**GlobalInstall** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Language** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Install-SPWebPartPack "MyCustomWebPartPack" -LiteralPath "c:/mywebpart.wpp" -GlobalInstall
```

This example installs the Web Part Package with the name  `MyCustomWebPartPack` globally in the farm from the path  `c:/mywebpart.wpp`.
  
## See also

#### 

[Uninstall-SPWebPartPack](uninstall-spwebpartpack.md)
  
[Get-SPWebPartPack](get-spwebpartpack.md)

