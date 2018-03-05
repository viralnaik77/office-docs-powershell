---
title: "Add-SPUserSolution"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 72503dc1-8926-4a11-825d-950398986195

description: "Uploads a new sandboxed solution to the solution gallery."
---

# Add-SPUserSolution

Uploads a new sandboxed solution to the solution gallery.
  
```
Add-SPUserSolution [-LiteralPath] <String> -Site <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Add-SPUserSolution** cmdlet uploads a new sandboxed solution package to the solution gallery. This cmdlet does not activate the uploaded sandboxed solution; to activate the solution in the site collection, use the **Install-SPUserSolution** cmdlet. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**LiteralPath** <br/> |Required  <br/> |System.String  <br/> |Specifies the path to the sandboxed solution package.  <br/> The type must be a valid path in either of the following forms:  <br/> - C:\folder_name  <br/> - \\server_name\folder_name  <br/> |
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the site collection where the sandboxed solution is to be added.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL, in the form http://server_name; or an instance of a valid **SPSite**object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**LiteralPath** <br/> |Required  <br/> |System.String  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Errors

|**Error**|**Description**|
|:-----|:-----|
|||
   
## Exceptions

|**Exceptions**|**Description**|
|:-----|:-----|
|||
   
## Example

-------------------EXAMPLE---------------------
  
```
Add-SPUserSolution -LiteralPath c:\contoso_solution.wsp -Site http://sitename
```

This example adds the sandboxed solution  `c:\contoso_solution.wsp` to the site  `http://sitename`.
  
## See also

#### 

[Update-SPUserSolution](update-spusersolution.md)
  
[Install-SPUserSolution](install-spusersolution.md)
  
[Uninstall-SPUserSolution](uninstall-spusersolution.md)
  
[Remove-SPUserSolution](remove-spusersolution.md)
  
[Get-SPUserSolution](get-spusersolution.md)

