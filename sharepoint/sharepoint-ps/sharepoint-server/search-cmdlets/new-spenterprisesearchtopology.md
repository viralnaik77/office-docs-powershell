---
title: "New-SPEnterpriseSearchTopology"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 2/11/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 60a5a81a-4c8a-47d6-8226-81b1e9d2fab9

description: "Creates a new search topology in the given search service application."
---

# New-SPEnterpriseSearchTopology

Creates a new search topology in the given search service application.
  
```
New-SPEnterpriseSearchTopology -SearchApplication <SearchServiceApplicationPipeBind> [-Clone <SwitchParameter>] [-SearchTopology <SearchTopologyPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE 1------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
New-SPEnterpriseSearchTopology -SearchApplication $ssa
```

This example creates a new, empty search topology in the search service application referenced by  `$ssa`.
  
------------------EXAMPLE 2------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
New-SPEnterpriseSearchTopology -SearchApplication $ssa -Clone -SearchTopology $topo
```

This example creates a new search topology in the search service application referenced by  `$ssa` by cloning the existing topology referenced by  `$topo`.
  
## Detailed Description

This cmdlet creates a new, inactive search topology in the given search service application. If the **Clone** switch is used, a cloned topology is created. Otherwise, an empty topology is created. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application to which the search topology will belong.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Clone_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the new search topology is to be created by cloning an existing search topology.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _SearchTopology_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchTopologyPipeBind  <br/> |Specifies the existing search topology of which the new topology will be a clone.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Clone** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SearchTopology** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchTopologyPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchTopology](get-spenterprisesearchtopology.md)
  
[Set-SPEnterpriseSearchTopology](set-spenterprisesearchtopology.md)
  
[Remove-SPEnterpriseSearchTopology](remove-spenterprisesearchtopology.md)
  
[Export-SPEnterpriseSearchTopology](export-spenterprisesearchtopology.md)
  
[Import-SPEnterpriseSearchTopology](import-spenterprisesearchtopology.md)

