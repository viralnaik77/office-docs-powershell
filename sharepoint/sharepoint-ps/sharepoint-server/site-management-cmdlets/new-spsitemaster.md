---
title: "New-SPSiteMaster"
ms.author: kirks
author: Techwriter40
ms.date: 6/3/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a8baf398-404d-4e0f-80d1-08ac8e37b7cf

description: "Creates a site master."
---

# New-SPSiteMaster

Creates a site master.
  
```
New-SPSiteMaster -ContentDatabase <SPContentDatabasePipeBind> -Template <SPWebTemplatePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-CompatibilityLevel <Int32>] [-Confirm [<SwitchParameter>]] [-Language <UInt32>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE-----------------------
  
```
New-SPSiteMaster -ContentDatabase WSS_Content -Template STS#0
```

This example creates a site master in the database WSS_Content.
  
## Detailed Description

Use the **New-SPSiteMaster** cmdlet to create a site master information in the farm. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ContentDatabase_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the name of the database to create the site master in. For example, WSS_Content.  <br/> |
| _Template_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebTemplatePipeBind  <br/> |Specifies the name of the template.  <br/> The values are the following:  <br/> **SPSPERS#2** <br/> **SPSPERS#6** <br/> **SPSPERS#7** <br/> **SPSPERS#8** <br/> **SPSPERS#9** <br/> **SPSPERS#10** <br/> **STS#0** <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CompatibilityLevel_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the version of templates to use when creating a new **SPSite** object. This value sets the initial CompatibilityLevel value for the site collection.  <br/>  When this parameter is not specified, the CompatibilityLevel will default to the highest possible version for the web application depending on the SiteCreationMode setting.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Language_ <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the locale ID to use. For example, use 1033 for English.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Get-SPSiteMaster](get-spsitemaster.md)
  
[Remove-SPSiteMaster](remove-spsitemaster.md)

