---
title: "Update-SPUserSolution"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d6d18298-aec4-4875-b6ce-69ce0f4a9600

description: "Upgrades an activated sandboxed solution in a farm."
---

# Update-SPUserSolution

Upgrades an activated sandboxed solution in a farm.
  
```
Update-SPUserSolution [-Identity] <SPUserSolutionPipeBind> -Site <SPSitePipeBind> -ToSolution <SPUserSolutionPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Update-SPUserSolution** cmdlet upgrades a sandboxed solution that has already been activated in a specified site collection. A user solution is a sandboxed solution. Before you use this cmdlet to upgrade the activated solution, use the **Add-SPUserSolution** cmdlet to upload the upgraded solution to the solution gallery. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserSolutionPipeBind  <br/> |Specifies the sandboxed solution to upgrade.  <br/> The type must be a valid name of a sandboxed solution (for example, UserSolution1); or an instance of a valid **SPUserSolution** object.  <br/> |
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Upgrade the sandboxed solution for the specified site collection.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL, in the form http://server_name; or an instance of a valid **SPSite** object.  <br/> |
|**ToSolution** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserSolutionPipeBind  <br/> |Specifies the sandboxed solution you want to upgrade to.  <br/> The type must be a valid name of a sandboxed solution (for example, UserSolution1); or an instance of a valid **SPUserSolution** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserSolutionPipeBind  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**ToSolution** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserSolutionPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE---------------------
  
```
Update-SPUserSolution -Identity contoso_solution.wsp -Site http://sitename -ToSolution contoso_solution_v2.wsp
```

This example upgrades the sandboxed solution  `contoso_solution.wsp` in the site  `http://sitename` to the sandboxed solution  `contoso_solution_v2.wsp`.
  
## See also

#### 

[Install-SPUserSolution](install-spusersolution.md)
  
[Uninstall-SPUserSolution](uninstall-spusersolution.md)
  
[Remove-SPUserSolution](remove-spusersolution.md)
  
[Get-SPUserSolution](get-spusersolution.md)
  
[Add-SPUserSolution](add-spusersolution.md)

