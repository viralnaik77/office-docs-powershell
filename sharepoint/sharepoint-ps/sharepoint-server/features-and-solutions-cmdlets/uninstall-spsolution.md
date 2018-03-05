---
title: "Uninstall-SPSolution"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/3/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc815ad1-cb94-4512-9ca2-891eb001f05b

description: "Retracts a deployed SharePoint solution."
---

# Uninstall-SPSolution

Retracts a deployed SharePoint solution.
  
```
Uninstall-SPSolution [-Identity] <SPSolutionPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-CompatibilityLevel <String>] [-Confirm [<SwitchParameter>]] [-Language <UInt32>] [-Local <SwitchParameter>] [-Time <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description
<a name="detail"> </a>

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Uninstall-SPSolution** cmdlet retracts a deployed SharePoint solution in preparation for removing it from the farm entirely. This cmdlet removes files from the front-end Web server. Use the **Remove-SPSolution** cmdlet to delete the solution package from the solution store of the farm; be sure to use the **Remove-SPSolution** cmdlet only after you have run **Uninstall-SPSolution**. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
The following table lists the valid values for the **CompatabilityLevel** parameter: 
  
|||
|:-----|:-----|
|**Value** <br/> |**Result** <br/> |
|**14** <br/> |Uninstalls solution from 14 directories only  <br/> |
|**16** <br/> |Uninstalls solution from 16 directories only  <br/> |
|**"14,16"** <br/> |Uninstalls solution from both 14 and 16 directories  <br/> |
|**"AllVersions" or "All"** <br/> |Uninstalls solution from both 14 and 16 directories  <br/> |
|**"OldVersions" or "Old"** <br/> |Uninstalls solution from 14 directories only  <br/> |
|**"NewVersion" or "New"** <br/> |Uninstalls solution from 16 directories only  <br/> |
   
## Parameters
<a name="detail"> </a>

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSolutionPipeBind  <br/> |Specifies the SharePoint solution to uninstall.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint solution (for example, SPSolution1); or an instance of a valid **SPSolution** object.  <br/> |
|**AllWebApplications** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the new SharePoint solution will be uninstalled for all SharePoint Web applications in the farm.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Uninstalls the SharePoint solution for the specified SharePoint Web application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of a SharePoint Web application (for example, MyOfficeApp1); or an instance of a valid **SPWebApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**CompatibilityLevel** <br/> |Optional  <br/> |System.String  <br/> |Specifies whether to uninstall the solution, from a specific version directory based on CompatibilityLevel. The default behavior if this parameter is not specified is to uninstall the solution only from the version directory based on the version tracked in the manifest of the solution's cab file. For the list of values, see the table in the [Detailed Description](#detail) section.  <br/> |
|**Language** <br/> |Optional  <br/> |System.UInt32  <br/> |Uninstalls the language pack for the specified language.  <br/> The type must be a valid language identifier; for example, 1033.  <br/> |
|**Local** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Uninstalls the solution from the active server computer.  <br/> |
|**Time** <br/> |Optional  <br/> |System.String  <br/> |Specifies when the solution will be uninstalled. The default value is immediate retraction.  <br/> The type must be a valid **DateTime** value, in the form 2010,12,05.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example
<a name="detail"> </a>

------------------EXAMPLE------------------
  
```
Uninstall-SPSolution -Identity contoso_solution.wsp
```

This example retracts the deployed SharePoint solution  `contoso_solution.wsp`.
  
## See also
<a name="detail"> </a>

#### 

[Get-SPSolution](get-spsolution.md)
  
[Add-SPSolution](add-spsolution.md)
  
[Update-SPSolution](update-spsolution.md)
  
[Remove-SPSolution](remove-spsolution.md)
  
[Install-SPSolution](install-spsolution.md)
  
[Remove-SPSolutionDeploymentLock](remove-spsolutiondeploymentlock.md)

