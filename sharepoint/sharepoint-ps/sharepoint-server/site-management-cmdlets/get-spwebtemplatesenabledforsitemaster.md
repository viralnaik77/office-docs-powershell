---
title: "Get-SPWebTemplatesEnabledForSiteMaster"
ms.author: kirks
author: Techwriter40
ms.date: 8/7/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 894731d4-7bc9-4f62-a31e-e0e6326b081e

description: "Returns a list of site master web templates."
---

# Get-SPWebTemplatesEnabledForSiteMaster

Returns a list of site master web templates.
  
```
Get-SPWebTemplatesEnabledForSiteMaster [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

------------------EXAMPLE-----------------------
  
```
Get-SPWebTemplatesEnabledForSiteMaster
```

This example displays all the site master web templates in a farm.
  
## Detailed Description

Use the **Get-SPWebTemplatesEnabledForSiteMaster** cmdlet to display a full list of site master web templates in the farm. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## See also

#### 

[Enable-SPWebTemplateForSiteMaster](enable-spwebtemplateforsitemaster.md)
  
[Disable-SPWebTemplateForSiteMaster](disable-spwebtemplateforsitemaster.md)

