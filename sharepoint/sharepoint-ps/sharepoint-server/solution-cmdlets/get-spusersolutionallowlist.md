---
title: "Get-SPUserSolutionAllowList"
ms.author: kirks
author: Techwriter40
ms.date: 9/13/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 554b8a3d-9b73-4cf9-bb0b-b5b8855bf3fd

description: "Gets the user managed solutions gallery configured on the specified web application."
---

# Get-SPUserSolutionAllowList

Gets the user managed solutions gallery configured on the specified web application.
  
```
Get-SPUserSolutionAllowList -WebApplication <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE 1------------------
  
```
$list = Get-SPUserSolutionAllowList -WebApplication http://localhost
```

This example gets the user managed solutions gallery on the web application with root http://localhost.
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _WebApplication_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the web application to search for the user solution allow list.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Disable-SPUserSolutionAllowList](disable-spusersolutionallowlist.md)
  
[New-SPUserSolutionAllowList](new-spusersolutionallowlist.md)
  
[Enable-SPUserSolutionAllowList](enable-spusersolutionallowlist.md)

