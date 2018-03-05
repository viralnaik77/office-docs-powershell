---
title: "Enable-SPFeature"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/12/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b68c192-b640-4cb8-8a92-a98008169b27

description: "Enables an installed SharePoint Feature at the given scope."
---

# Enable-SPFeature

Enables an installed SharePoint Feature at the given scope.
  
```
Enable-SPFeature [-Identity] <SPFeatureDefinitionPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-CompatibilityLevel <Int32>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-PassThru <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Enable-SPFeature** cmdlet enables an installed feature at the given scope. If the feature is a farm feature, no URL is needed. Otherwise, provide the URL where the feature is to be enabled and it will be enabled at the proper scope based on the Feature definition. 
  
This cmdlet has no output unless the **PassThru** parameter is provided, in which case the **SPFeatureDefinition** object for the newly enabled feature is returned. 
  
> [!NOTE]
> If you try to use the **Url** parameter on a farm-scoped feature, you receive the following error message: > The feature '<feature name>' applies to the entire farm; the **Url** parameter cannot be used with farm-scoped features. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPFeatureDefinitionPipeBind  <br/> |Specifies the name of the Feature or GUID to enable.  <br/> The type must be the name of the Feature folder located in the 14\Template\Features folder or GUID, in the form 21d186e1-7036-4092-a825-0eb6709e9281.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CompatibilityLevel** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the version of templates to use when creating a new **SPSite** object. This value sets the initial CompatibilityLevel value for the site collection. When this parameter is not specified, the CompatibilityLevel will default to the highest possible version for the web application depending on the CompatibilityRange setting.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forces the activation of a Feature. This causes any custom code associated with the Feature to rerun.  <br/> |
|**PassThru** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |If provided, the cmdlet outputs the Feature definition object after enable.  <br/> |
|**Url** <br/> |Optional  <br/> |System.String  <br/> |Specifies the URL of the Web application, site collection, or Web site for which the Feature is being activated.  <br/> The type must be a valid URL; for example, http://server_name.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

--------------EXAMPLE 1-----------------
  
```
Enable-SPFeature -identity "MyCustom" -URL http://somesite
```

This example enables the  `"MyCustom"` site scoped SharePoint Feature at  `http://somesite`.
  
--------------EXAMPLE 2-----------------
  
```
$w = Get-SPWeb http://somesite/myweb | ForEach{ $_.URL }
```

```
Get-SPFeature -Web $w |%{ Enable-SPFeature -Identity $_ -URL $w}
```

This example enables all SharePoint Features in the subsite at  `http://somesite/myweb`.
  
## See also

#### 

[Disable-SPFeature](disable-spfeature.md)
  
[Install-SPFeature](install-spfeature.md)
  
[Uninstall-SPFeature](uninstall-spfeature.md)
  
[Get-SPFeature](get-spfeature.md)

