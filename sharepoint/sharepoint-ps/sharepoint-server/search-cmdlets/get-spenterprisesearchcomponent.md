---
title: "Get-SPEnterpriseSearchComponent"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e0342473-a608-4745-b5ea-7b7c812b2ba2

description: "Retrieves one or all search components in a given search topology."
---

# Get-SPEnterpriseSearchComponent

Retrieves one or all search components in a given search topology.
  
```
Get-SPEnterpriseSearchComponent -SearchTopology <SearchTopologyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <SearchComponentPipeBind>] [-SearchApplication <SearchServiceApplicationPipeBind>]

```

## Example

------------------EXAMPLE 1-----------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
```

```
Get-SPEnterpriseSearchComponent -SearchTopology 56e6651d-ecdd-4105-bb65-6a83b6155525 -Identity 06e6651d-ecdd-4105-bb65-6a83b6155525 -SearchApplication $ssa
```

This example retrieves the search component with the identity  `06e6651d-ecdd-4105-bb65-6a83b6155525` from the search topology with identity  `56e6651d-ecdd-4105-bb65-6a83b6155525` in the search service application referenced by  `$ssa`.
  
------------------EXAMPLE 2-----------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
```

```
Get-SPEnterpriseSearchComponent -SearchTopology 56e6651d-ecdd-4105-bb65-6a83b6155525 -SearchApplication $ssa
```

This example retrieves all search components from the search topology with the identity  `56e6651d-ecdd-4105-bb65-6a83b6155525` in the search service application referenced by  `$ssa`.
  
## Detailed Description

This cmdlet retrieves the search component with the specified identity from the given search topology. If an identity is not provided, all search components in the given search topology will be retrieved.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchTopology_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchTopologyPipeBind  <br/> |Specifies the search topology from which to retrieve the search component/search components.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchComponentPipeBind  <br/> |Specifies the identity for a search component.  <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search service application that contains the search topology and search component/search components.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchComponentPipeBind  <br/> ||
|**SearchTopology** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchTopologyPipeBind  <br/> |Specifies the search service application that contains the search topology and search components/search components  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
   

