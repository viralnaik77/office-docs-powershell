---
title: "Uninstall-SPUserSolution"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 21c7f50f-a177-4cd3-b1e9-dcdd70062a85

description: "Deactivates a sandboxed solution in a site collection."
---

# Uninstall-SPUserSolution

Deactivates a sandboxed solution in a site collection.
  
```
Uninstall-SPUserSolution [-Identity] <SPUserSolutionPipeBind> -Site <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Uninstall-SPUserSolution** cmdlet deactivates a sandboxed solution in a site collection so that you can delete it by using the **Remove-SPUserSolution** cmdlet. A user solution is a sandboxed solution. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserSolutionPipeBind  <br/> |Specifies the sandboxed solution to deactivate.  <br/> The type must be a valid name of a sandboxed solution (for example, UserSolution1); or an instance of a valid **SPUserSolution** object.  <br/> |
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Deactivates the sandboxed solution for the specified site collection.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL, in the form http://server_name; or an instance of a valid **SPSite** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserSolutionPipeBind  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE--------------- 
  
```
Uninstall-SPUserSolution -Identity contoso_solution.wsp -Site http://sitename
```

This example deactivates the sandboxed solution  `contoso_solution.wsp` on the site  `http://sitename`.
  
## See also

#### 

[Update-SPUserSolution](update-spusersolution.md)
  
[Install-SPUserSolution](install-spusersolution.md)
  
[Remove-SPUserSolution](remove-spusersolution.md)
  
[Get-SPUserSolution](get-spusersolution.md)
  
[Add-SPUserSolution](add-spusersolution.md)

