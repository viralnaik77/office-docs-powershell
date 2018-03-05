---
title: "Disable-SPWebTemplateForSiteMaster"
ms.author: kirks
author: Techwriter40
ms.date: 10/23/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 002bc6aa-358f-4207-be32-a777c9c30693

description: "Disables the site master in the farm."
---

# Disable-SPWebTemplateForSiteMaster

Disables the site master in the farm.
  
```
Disable-SPWebTemplateForSiteMaster -Template <SPWebTemplatePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-CompatibilityLevel <Int32>]

```

## Example

------------------EXAMPLE-----------------------
  
```
Disable-SPWebTemplateForSiteMaster -Template STS#0
```

This example disables the template in the site master of a farm.
  
## Detailed Description

Use the **Disable-SPWebTemplateForSiteMaster** cmdlet to disable a site master in the farm. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Template_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebTemplatePipeBind  <br/> | Specifies the name of the template.  <br/>  The values are the following:  <br/>  SPSPERS#2  <br/>  SPSPERS#6  <br/>  SPSPERS#7  <br/>  SPSPERS#8  <br/>  SPSPERS#9  <br/>  SPSPERS#10  <br/>  STS#0  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CompatibilityLevel_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the version of templates to use when creating a new **SPSite** object. This value sets the initial CompatibilityLevel value for the site collection.  <br/>  When this parameter is not specified, the **CompatibilityLevel** parameter will default to the highest possible version for the web application depending on the SiteCreationMode setting.  <br/> |
   
## See also

#### 

[Get-SPWebTemplatesEnabledForSiteMaster](get-spwebtemplatesenabledforsitemaster.md)
  
[Enable-SPWebTemplateForSiteMaster](enable-spwebtemplateforsitemaster.md)

