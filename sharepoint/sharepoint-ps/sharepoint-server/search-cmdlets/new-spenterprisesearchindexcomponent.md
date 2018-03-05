---
title: "New-SPEnterpriseSearchIndexComponent"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b2ad4e49-d34f-4a59-aa19-9a79f536f830

description: "Creates a new index component for the given topology and search service instance."
---

# New-SPEnterpriseSearchIndexComponent

Creates a new index component for the given topology and search service instance.
  
```
New-SPEnterpriseSearchIndexComponent -SearchServiceInstance <SearchServiceInstancePipeBind> -SearchTopology <SearchTopologyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-IndexPartition <UInt32>] [-RootDirectory <String>] [-SearchApplication <SearchServiceApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE-----------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
```

```
New-SPEnterpriseSearchIndexComponent -SearchTopology 06e6651d-ecdd-4105-bb65-6a83b6155525 -SearchServiceInstance 56e6651d-ecdd-4105-bb65-6a83b6155525 -SearchApplication $ssa -IndexPartition 1 -RootDirectory E:\Index
```

This example adds a new search index component to the search topology with identity  `06e6651d-ecdd-4105-bb65-6a83b6155525` in the search service instance with identity  `56e6651d-ecdd-4105-bb65-6a83b6155525` in the default search service application referenced by  `$ssa`, with index partition  `1` and root directory  `E:\Index`.
  
## Detailed Description

Creates a new index component and adds it to an inactive search topology in a specific search service instance. The change is effectuated when the search topology is enabled.
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchServiceInstance_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceInstancePipeBind  <br/> |Specifies the search service instance that will host the new index component. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid name of a search topology server, or an instance of a valid **SearchServiceInstance** object.  <br/> |
| _SearchTopology_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchTopologyPipeBind  <br/> |Specifies the search topology where the new index component should be added.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _IndexPartition_ <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the index partition number to assign to the new search index component.  <br/> |
| _RootDirectory_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the root directory that will hold the index location for the new search index component. This is needed if you want to isolate the index on dedicated discs in order to avoid I/O contention with other parts of the system, other system sharing the same disks, or because you do not want to risk the index filling up the OS disk (generally C: )  <br/> > [!NOTE]> If you specify the root directory to be the root of a volume, e.g. E:, the index will not be cleaned up if you delete the SSA. You will then have to delete the index files manually.           > [!CAUTION]> You can't enter the same root directory for multiple index components on the same server. If you are adding a new index component that represents an index replica of an index partition, specify a different root directory location for each index component that you add. If you use the same root directory for multiple index components, your search index may get corrupted.           |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search service application that contains the search topology.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SearchServiceInstance** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceInstancePipeBind  <br/> ||
|**SearchTopology** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchTopologyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**IndexPartition** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**RootDirectory** <br/> |Optional  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   

