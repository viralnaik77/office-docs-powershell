---
title: "Disable-SPFeature"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c10fbc69-088c-4e49-9005-fde54c035f23

description: "Disables an installed SharePoint Feature at a given scope."
---

# Disable-SPFeature

Disables an installed SharePoint Feature at a given scope.
  
```
Disable-SPFeature [-Identity] <SPFeatureDefinitionPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-Url <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Disable-SPFeature** cmdlet disables a SharePoint Feature at the given scope. If the scope of the Feature is the farm, the URL is not needed. Otherwise, provide the URL at which this Feature is to be deactivated (explicit scope is not needed). 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPFeatureDefinitionPipeBind  <br/> |Specifies the name of the Feature or GUID to disable.  <br/> The type must be the name of the Feature folder located in the 14\Template\Features folder or GUID, in the format 21d186e1-7036-4092-a825-0eb6709e9281.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forces a Feature to be disabled.  <br/> |
|**Url** <br/> |Optional  <br/> |System.String  <br/> |Specifies the URL of the Web application, site collection, or Web site to which the Feature is being disabled.  <br/> The type must be a valid URL, such as http://server_name.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Return Types

none
  
## Example

--------------EXAMPLE 1-----------------
  
```
Disable-SPFeature -identity "MyCustom" -URL http://somesite
```

This example disables the  `"MyCustom"` Web site scoped feature at  `http://somesite`.
  
--------------EXAMPLE 2-----------------
  
```
$w = Get-SPWeb http://somesite/myweb | ForEach{ $_.URL }
```

```
Get-SPFeature -Web $w |%{ Disable-SPFeature -Identity $_ -URL $w}
```

This example disables all features in the subsite at  `http://somesite/myweb`.
  
You do not need to use the **SPAssignment** cmdlets in this case because the Web object is not stored — only the string value for the URL. 
  
## See also

#### 

[Install-SPFeature](install-spfeature.md)
  
[Enable-SPFeature](enable-spfeature.md)
  
[Get-SPFeature](get-spfeature.md)
  
[Uninstall-SPFeature](uninstall-spfeature.md)

