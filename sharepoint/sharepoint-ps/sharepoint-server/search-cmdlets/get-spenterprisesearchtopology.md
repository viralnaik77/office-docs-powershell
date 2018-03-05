---
title: "Get-SPEnterpriseSearchTopology"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 43e2c839-54b8-4f78-b883-abc1dbea617c

description: "Retrieves one or all search topologies that belong to a given search service application."
---

# Get-SPEnterpriseSearchTopology

Retrieves one or all search topologies that belong to a given search service application.
  
```
Get-SPEnterpriseSearchTopology -SearchApplication <SearchServiceApplicationPipeBind> [-Active <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>] [-Identity <SearchTopologyPipeBind>]

```

## Example

------------------EXAMPLE 1------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
```

```
Get-SPEnterpriseSearchTopology -SearchApplication $ssa
```

This example retrieves all search topologies of the search service application referenced by  `$ssa`.
  
------------------EXAMPLE 2------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
```

```
Get-SPEnterpriseSearchTopology -SearchApplication $ssa -Active
```

This example retrieves the active search topology of the search service application referenced by  `$ssa`.
  
------------------EXAMPLE 3------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication

```

```
Get-SPEnterpriseSearchTopology -SearchApplication $ssa -Identity 10fa59cb-4b32-4fe6-8f8d-065388df201e
```

This example retrieves search topology with the identity  `10fa59cb-4b32-4fe6-8f8d-065388df201e` of the search service application referenced by  `$ssa`.
  
## Detailed Description

This cmdlet retrieves a given search topology, the active search topology, or all search topologies that belong to a given search service application.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application to which the search topology belongs.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _Active_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the active search topology should be returned.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchTopologyPipeBind  <br/> |Specifies the search topology to retrieve.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchTopologyPipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**Active** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchTopology](new-spenterprisesearchtopology.md)
  
[Set-SPEnterpriseSearchTopology](set-spenterprisesearchtopology.md)
  
[Remove-SPEnterpriseSearchTopology](remove-spenterprisesearchtopology.md)
  
[Export-SPEnterpriseSearchTopology](export-spenterprisesearchtopology.md)
  
[Import-SPEnterpriseSearchTopology](import-spenterprisesearchtopology.md)

