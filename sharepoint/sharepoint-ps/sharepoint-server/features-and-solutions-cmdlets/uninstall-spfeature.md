---
title: "Uninstall-SPFeature"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2f3831e4-b964-4e0e-bcc5-02659fdc0bb7

description: "Uninstalls an installed feature definition."
---

# Uninstall-SPFeature

Uninstalls an installed feature definition.
  
```
Uninstall-SPFeature [-Identity] <SPFeatureDefinitionPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-CompatibilityLevel <Int32>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Uninstall-SPFeature** cmdlet removes the specified feature definition from the collection of feature definitions in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Parameter  <br/> |Microsoft.SharePoint.PowerShell.SPFeatureDefinitionPipeBind  <br/> |Specifies the name of the feature or GUID to uninstall.  <br/> The type must be the name of the feature folder located in the  _\<drive\>_:\program files\common files\Microsoft Shared\Web server extensions\16\template\features folder, or must be a GUID, in the form 21d186e1-7036-4092-a825-0eb6709e9281.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CompatibilityLevel** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the version of feature to uninstall. When the version is not specified it will default to the web applications MaxVersion value.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |No  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forces the uninstallation of a feature that is already installed.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

------------------EXAMPLE 1-----------------------
  
```
Uninstall-SPFeature -Identity "MyCustomFeature"
```

This example uninstalls the feature at $env:ProgramFiles\Common Files\Microsoft Shared\Web Server Extensions\16\TEMPLATE\FEATURES\ `MyCustomFeature`/feature.xml.
  
------------------EXAMPLE 2-----------------------
  
```
Uninstall-SPFeature -Identity "MyCustomFeature" -CompatibilityLevel 14
```

This example uninstalls the feature at $env:ProgramFiles\Common Files\Microsoft Shared\Web Server Extensions\16\TEMPLATE\FEATURES\ `MyCustomFeature`/feature.xml.
  
## See also

#### 

[Get-SPFeature](get-spfeature.md)
  
[Enable-SPFeature](enable-spfeature.md)
  
[Disable-SPFeature](disable-spfeature.md)
  
[Install-SPFeature](install-spfeature.md)

