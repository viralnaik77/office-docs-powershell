---
title: "Update-SPSolution"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/3/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7748591a-b137-48a2-84dd-fdd7727a938e

description: "Upgrades a deployed SharePoint solution."
---

# Update-SPSolution

Upgrades a deployed SharePoint solution.
  
```
Update-SPSolution [-Identity] <SPSolutionPipeBind> -LiteralPath <String> [-AssignmentCollection <SPAssignmentCollection>] [-CASPolicies <SwitchParameter>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-FullTrustBinDeployment <SwitchParameter>] [-GACDeployment <SwitchParameter>] [-Local <SwitchParameter>] [-Time <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Update-SPSolution** cmdlet upgrades a deployed SharePoint solution in the farm. Use this cmdlet only if a new solution contains the same set of files and features as the deployed solution. If files and features are different, the solution must be retracted and redeployed by using the **Uninstall-SPSolution** and **Install-SPSolution** cmdlets, respectively. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSolutionPipeBind  <br/> |Specifies the SharePoint solution to deploy.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint solution (for example, SPSolution1); or an instance of a valid **SPSolution** object.  <br/> |
|**LiteralPath** <br/> |Required  <br/> |System.String  <br/> |Specifies the path to the solution package.  <br/> The type must be a valid path in either of the following forms:  <br/> - C:\folder_name  <br/> - \\server_name\folder_name  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CASPolicies** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that Code Access Security (CAS) policies can be deployed for the new SharePoint solution.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forces the deployment of the new SharePoint solution.  <br/> |
|**FullTrustBinDeployment** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether to deploy using fully trusted bin.  <br/> |
|**GACDeployment** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the new SharePoint solution can be deployed to the global assembly cache (GAC).  <br/> |
|**Local** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Deploys the solution on the local computer only.  <br/> |
|**Time** <br/> |Optional  <br/> |System.String  <br/> |Specifies when the solution will be deployed. The default value is immediate deployment.  <br/> The type must be a valid **DateTime** string, in the form YYYY-MM-DD ("2014-3-3") or MM-DD-YYYY ("3-3-2014").  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSolutionPipeBind  <br/> ||
|**LiteralPath** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CASPolicies** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**FullTrustBinDeployment** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**GACDeployment** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Local** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Time** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Update-SPSolution -Identity contoso_solution.wsp -LiteralPath c:\contoso_solution_v2.wsp -GACDeployment
```

This example upgrades the deployed SharePoint solution  `contoso_solution.wsp` to the solution  `c:\contoso_solution_v2.wsp`.
  
## See also

#### 

[Get-SPSolution](get-spsolution.md)
  
[Add-SPSolution](add-spsolution.md)
  
[Uninstall-SPSolution](uninstall-spsolution.md)
  
[Remove-SPSolution](remove-spsolution.md)
  
[Install-SPSolution](install-spsolution.md)
  
[Remove-SPSolutionDeploymentLock](remove-spsolutiondeploymentlock.md)

