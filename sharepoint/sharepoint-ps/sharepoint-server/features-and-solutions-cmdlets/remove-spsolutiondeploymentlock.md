---
title: "Remove-SPSolutionDeploymentLock"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/3/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86f565a3-0a23-48d3-b50a-296982041dd7

description: "Removes the solution deployment lock for a server."
---

# Remove-SPSolutionDeploymentLock

Removes the solution deployment lock for a server.
  
```
Remove-SPSolutionDeploymentLock [[-Identity] <SPServerPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPSolutionDeploymentLock** cmdlet removes the solution deployment lock for a server. If the **Identity** parameter is not specified, this cmdlet removes the solution deployment lock for all servers in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServerPipeBind  <br/> |Specifies the server for which the solution deployment lock is to be removed.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; the IP address of a server computer, in the form 208.77.188.166; a valid name of a SQL Server host service (for example, SQLServerHost1); or an instance of a valid **SPServer** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServerPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Remove-SPSolutionDeploymentLock
```

This example removes the solution deployment lock for all servers in the farm.
  
## See also

#### 

[Remove-SPSolution](remove-spsolution.md)
  
[Get-SPSolution](get-spsolution.md)
  
[Add-SPSolution](add-spsolution.md)
  
[Update-SPSolution](update-spsolution.md)
  
[Uninstall-SPSolution](uninstall-spsolution.md)
  
[Install-SPSolution](install-spsolution.md)

