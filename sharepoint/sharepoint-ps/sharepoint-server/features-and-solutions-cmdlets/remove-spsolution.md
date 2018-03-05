---
title: "Remove-SPSolution"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/3/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 862985c6-480b-49e7-926b-8497235bcba2

description: "Removes a SharePoint solution from a farm."
---

# Remove-SPSolution

Removes a SharePoint solution from a farm.
  
```
Remove-SPSolution [-Identity] <SPSolutionPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-Language <UInt32>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPSolution** cmdlet deletes a SharePoint solution from a farm. Before you use this cmdlet, you must use the **Uninstall-SPSolution** cmdlet to retract the solution files from the front-end Web server. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSolutionPipeBind  <br/> |Specifies the SharePoint solution to remove.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint solution (for example, SPSolution1); or an instance of a valid **SPSolution** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forces the removal of the SharePoint solution. You can use this parameter to remove SharePoint solutions that have been added to the server, even if they have not been deployed by using the **Install-SPSolution** cmdlet.  <br/> |
|**Language** <br/> |Optional  <br/> |System.UInt32  <br/> |Removes the language pack for the specified language.  <br/> The type must be a valid language identifier; for example, 1033.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

------------------EXAMPLE------------------
  
```
Remove-SPSolution -Identity contoso_solution.wsp
```

This example removes the SharePoint solution  `contoso_solution.wsp`.
  
## See also

#### 

[Get-SPSolution](get-spsolution.md)
  
[Add-SPSolution](add-spsolution.md)
  
[Update-SPSolution](update-spsolution.md)
  
[Uninstall-SPSolution](uninstall-spsolution.md)
  
[Install-SPSolution](install-spsolution.md)

