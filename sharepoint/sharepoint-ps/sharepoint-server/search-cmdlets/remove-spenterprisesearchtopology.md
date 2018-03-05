---
title: "Remove-SPEnterpriseSearchTopology"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 15289d89-02bb-4d34-abf8-6fb217ffe341

description: "Removes an inactive search topology from a search service application."
---

# Remove-SPEnterpriseSearchTopology

Removes an inactive search topology from a search service application.
  
```
Remove-SPEnterpriseSearchTopology -Identity <SearchTopologyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-SearchApplication <SearchServiceApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE 1------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
```

```
$topology = Get-SPEnterpriseSearchTopology -SearchApplication $ssa -Identity 4b32-4fe6-8f8d-065388df201e
```

```
Remove-SPEnterpriseSearchTopology -Identity $topology
```

This example removes a search topology with the identity  `4b32-4fe6-8f8d-065388df201e`.
  
------------------EXAMPLE 2------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication

```

```
Remove-SPEnterpriseSearchTopology -Identity $topo -SearchApplication $ssa
```

This example removes the search topology referenced by  `$topo` in the search service application referenced by  `$ssa`.
  
## Detailed Description

This cmdlet removes the given inactive search topology from the search service application to which it belongs.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchTopologyPipeBind  <br/> |Specifies the search topology to retrieve.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application to which the search topology belongs.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchTopologyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchTopology](get-spenterprisesearchtopology.md)
  
[New-SPEnterpriseSearchTopology](new-spenterprisesearchtopology.md)
  
[Set-SPEnterpriseSearchTopology](set-spenterprisesearchtopology.md)
  
[Export-SPEnterpriseSearchTopology](export-spenterprisesearchtopology.md)
  
[Import-SPEnterpriseSearchTopology](import-spenterprisesearchtopology.md)

