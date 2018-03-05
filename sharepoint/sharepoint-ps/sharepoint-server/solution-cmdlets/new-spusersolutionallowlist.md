---
title: "New-SPUserSolutionAllowList"
ms.author: kirks
author: Techwriter40
ms.date: 9/13/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8a5e186f-77d0-40b3-ae99-c847b52defc6

description: "Creates a user managed solutions gallery."
---

# New-SPUserSolutionAllowList

Creates a user managed solutions gallery.
  
```
New-SPUserSolutionAllowList -ListTitle <String> -Site <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE 1------------------
  
```
$list = New-SPUserSolutionAllowList -Site http://localhost/sites/site1 -ListTitle "Allow List"
```

This example creates a user managed solutions gallery named "Allow List" under the root web of the site collection at http://localhost/sites/site1.
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ListTitle_ <br/> |Required  <br/> |System.String  <br/> |Specifies the title of the user solution allow list to create.  <br/> |
| _Site_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the site collection where the user solution allow list will be created.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Get-SPUserSolutionAllowList](get-spusersolutionallowlist.md)
  
[Disable-SPUserSolutionAllowList](disable-spusersolutionallowlist.md)
  
[Enable-SPUserSolutionAllowList](enable-spusersolutionallowlist.md)

