---
title: "Install-SPSolution"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0133c53b-70c4-4dff-a2ae-3c94759ed25d

description: "Deploys an installed SharePoint solution in the farm."
---

# Install-SPSolution

Deploys an installed SharePoint solution in the farm.
  
```
Install-SPSolution [-Identity] <SPSolutionPipeBind> [-AllWebApplications <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>] [-CASPolicies <SwitchParameter>] [-CompatibilityLevel <String>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-FullTrustBinDeployment <SwitchParameter>] [-GACDeployment <SwitchParameter>] [-Language <UInt32>] [-Local <SwitchParameter>] [-Time <String>] [-WebApplication <SPWebApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description
<a name="detail"> </a>

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Install-SPSolution** cmdlet deploys an installed SharePoint solution in the farm. Use the **Add-SPSolution** cmdlet to install a SharePoint solution package in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
The following table lists the valid values for the **CompatabilityLevel** parameter: 
  
|||
|:-----|:-----|
|**Value** <br/> |**Result** <br/> |
|**14** <br/> |Installs solution to 14 directories only  <br/> |
|**16** <br/> |Installs solution to 16 directories only  <br/> |
|**"14,16"** <br/> |Installs solution to both 14 and 16 directories  <br/> |
|**"AllVersions" or "All"** <br/> |Installs solution to both 14 and 16 directories  <br/> |
|**"OldVersions" or "Old"** <br/> |Installs solution to 14 directories only  <br/> |
|**"NewVersion" or "New"** <br/> |Installs solution to 16 directories only  <br/> |
   
## Parameters
<a name="detail"> </a>

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSolutionPipeBind  <br/> |Specifies the SharePoint solution to deploy.  <br/> The value must be an authentic GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; an authentic name of a SharePoint solution (for example, SPSolution1); or an instance of an authentic **SPSolution** object.  <br/> |
|**AllWebApplications** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the new SharePoint solution is deployed for all SharePoint web applications in the farm.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CASPolicies** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that code access security (CAS) policies can be deployed for the new SharePoint solution.  <br/> |
|**CompatibilityLevel** <br/> |Optional  <br/> |System.String  <br/> |Specifies whether to install into the solution, into a specific version directory based on CompatibilityLevel. The default behavior if this parameter is not specified is to install the solution only to the version directory based on the version tracked in the manifest of the solution's cab file. For the list of values, see the table in the [Detailed Description](#detail) section.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forces the deployment of the new SharePoint solution.  <br/> |
|**FullTrustBinDeployment** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that full trust Bin deployment is permitted. This parameter is to be used if the solution is fully trusted.  <br/> Bin assembly is an assembly installed into the bin directory of the virtual server. The assembly in the package will have DeploymentTarget=WebApplication attribute set. For additional information about bin assembly, see [Assembly Element](https://technet.microsoft.com/en-us/library/ms468837.aspx) <br/> |
|**GACDeployment** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that global assembly cache (GAC) can be deployed for the new SharePoint solution.  <br/> |
|**Language** <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies a language for the solution when a solution language package is deployed. If this parameter is not specified, zero ("0") is assumed. Use zero for solutions that are valid for all languages.  <br/> |
|**Local** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Deploys the solution on the active server.  <br/> |
|**Synchronize** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Synchronizes all solutions or the specified solution in the local farm.  <br/> |
|**Time** <br/> |Optional  <br/> |System.String  <br/> |Specifies when the solution will be deployed. The default value is immediate deployment.  <br/> The type must be a valid **DateTime** value, in the form 2010, 5, 1.  <br/> |
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> | Deploys the SharePoint solution for the specified SharePoint web application.  <br/>  The value must be in one of the following forms:  <br/>  An authentic GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh  <br/>  An authentic name of a SharePoint web application (for example, MyOfficeApp1)  <br/>  An instance of an authentic **SPWebApplication** object.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams
<a name="detail"> </a>

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSolutionPipeBind  <br/> ||
|**Synchronize** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AllWebApplications** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CASPolicies** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**CompatibilityLevel** <br/> |Optional  <br/> |System.String  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**FullTrustBinDeployment** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**GACDeployment** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Language** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**Local** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Time** <br/> |Optional  <br/> |System.String  <br/> ||
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example
<a name="detail"> </a>

------------------EXAMPLE 1------------------
  
```
Install-SPSolution -Identity contoso_solution.wsp -GACDeployment
```

This example deploys the installed SharePoint solution  `contoso_solution.wsp` in the farm and specifies that GAC can be deployed for the new SharePoint solution. 
  
------------------EXAMPLE 2------------------
  
```
Install-SPSolution -Identity contoso_solution.wsp -GACDeployment -CompatibilityLevel 15
```

This example deploys the installed SharePoint solution  `contoso_solution.wsp` in the farm within the latest version directories and specifies that global assembly cache (GAC) can be deployed for the new SharePoint solution. 
  
------------------EXAMPLE 3------------------
  
```
Install-SPSolution -Identity contoso_solution.wsp -GACDeployment -CompatibilityLevel {14,15}
```

This example deploys the installed SharePoint solution installs a previously added solution so it can be used correctly in both 14 and 15 mode site collections.
  
## See also
<a name="detail"> </a>

#### 

[Get-SPSolution](get-spsolution.md)
  
[Add-SPSolution](add-spsolution.md)
  
[Update-SPSolution](update-spsolution.md)
  
[Uninstall-SPSolution](uninstall-spsolution.md)
  
[Remove-SPSolution](remove-spsolution.md)
  
[Remove-SPSolutionDeploymentLock](remove-spsolutiondeploymentlock.md)

