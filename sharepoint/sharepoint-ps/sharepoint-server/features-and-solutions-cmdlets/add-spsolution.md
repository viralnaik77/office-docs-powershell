---
title: "Add-SPSolution"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/1/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c64c1ac-39c0-4d5e-923f-27d0c48b006a

description: "Uploads a SharePoint solution package to the farm."
---

# Add-SPSolution

Uploads a SharePoint solution package to the farm.
  
```
Add-SPSolution [-LiteralPath] <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Language <UInt32>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Add-SPSolution** cmdlet adds a SharePoint solution package to the farm. This cmdlet does not deploy the uploaded SharePoint solution. Use the **Install-SPSolution** cmdlet to deploy the SharePoint solution in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**LiteralPath** <br/> |Required  <br/> |System.String  <br/> |Specifies the path to the solution package.  <br/> The type must be a valid path in either of the following forms:  <br/> - C:\folder_name  <br/> - \\server_name\folder_name  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Language** <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the language pack to install with the solution package.  <br/> The type must be a valid language identifier; for example, 1033.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**LiteralPath** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Language** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Add-SPSolution -LiteralPath c:\contoso_solution.wsp
```

This example adds the SharePoint solution in the file  `contoso_solution.wsp` to the farm. 
  
## See also

#### 

[Get-SPSolution](get-spsolution.md)
  
[Update-SPSolution](update-spsolution.md)
  
[Uninstall-SPSolution](uninstall-spsolution.md)
  
[Remove-SPSolution](remove-spsolution.md)
  
[Install-SPSolution](install-spsolution.md)
  
[Remove-SPSolutionDeploymentLock](remove-spsolutiondeploymentlock.md)

