---
title: "Install-SPFeature"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a1093d30-68a1-4c84-8454-967bda8d68b9

description: "Installs a SharePoint Feature by using the Feature.xml file."
---

# Install-SPFeature

Installs a SharePoint Feature by using the Feature.xml file.
  
```
Install-SPFeature [-Path] <String> [-AssignmentCollection <SPAssignmentCollection>] [-CompatibilityLevel <Int32>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Install-SPFeature** cmdlet installs a specific **SPFeature** by providing, in the **Identity** parameter, the relative path from the version-specific common FEATURES folder to the feature. The version-specific FEATURES folder is "$env:ProgramFiles\Common Files\Microsoft Shared\Web Server Extensions\14\TEMPLATE\FEATURES\" if the site collection is in 14 mode, and "$env:ProgramFiles\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\" if the site collection is in 15 mode. The SharePoint Feature's files must already be put in the proper directory, either manually or by using a solution installer. 
  
If the value of the **AllExistingFeatures** parameter is true, the file system is scanned and all new features that are in both FEATURES folders are installed. This is generally only used during deployment and upgrade. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies an authentic file path; for example, MyFeature.  <br/> The path to feature must be a literal path to the 14\Template\Features directory. The feature.xml file name is implied and does not need to be provided.  <br/> If the path to the feature is not found , the following error message is displayed: "Failed to find the XML file at location 14\Template\Features\\<file path\>."  <br/> |
|**AllExistingFeatures** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Scans for existing, but unregistered features, and then registers them with the farm.  <br/> |
|**ScanForFeatures** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Scans and then displays a feature. The **ScanForFeatures** parameter does not install a feature.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CompatibilityLevel** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the version of feature to install. When the version is not specified it will default to the web applications MaxVersion value.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forces the installation of an already installed feature.  <br/> |
|**SolutionId** <br/> |Optional  <br/> |System.String  <br/> |Specifies the solution ID of the features. If the **SolutionId** parameter is not provided, all solution IDs are scanned.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

--------------EXAMPLE 1-----------------
  
```
Install-SPFeature -path "MyCustomFeature"
```

This example installs a new feature at $env:ProgramFiles\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\ `MyCustomFeature`/feature.xml.
  
--------------EXAMPLE 2-----------------
  
```
Install-SPFeature -AllExistingFeatures -Whatif
```

This example shows the unregistered features that are available on the file system and that are installed if this command is run without the  `WhatIf` parameter. This is commonly done after an upgrade process. 
  
## See also

#### 

[Get-SPFeature](get-spfeature.md)
  
[Enable-SPFeature](enable-spfeature.md)
  
[Disable-SPFeature](disable-spfeature.md)
  
[Uninstall-SPFeature](uninstall-spfeature.md)

