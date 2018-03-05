---
title: "Get-SPEnterpriseSearchHostController"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d93675ff-d1fc-4a01-8506-9e29ce22db1d

description: "Lists the specified or all search host controllers in the farm."
---

# Get-SPEnterpriseSearchHostController

Lists the specified or all search host controllers in the farm.
  
```
Get-SPEnterpriseSearchHostController [-AssignmentCollection <SPAssignmentCollection>] [-SearchServiceInstance <SearchServiceInstancePipeBind>]

```

## Example

------------------EXAMPLE 1------------------
  
```
Get-SPEnterpriseSearchHostController
```

This example retrieves a list of all HostControllers in the farm with their status (primary/secondary) and repository version.
  
------------------EXAMPLE 2------------------
  
```
$ssi = Get-SPEnterpriseSearchServiceInstance -Local

```

```
Get-SPEnterpriseSearchHostController -SearchServiceInstance $ssi
```

This example retrieves the status information for the **SearchHostController** on the local server. 
  
## Detailed Description

This cmdlet lists the specified or all **SearchHostControllers** in the farm. The **SearchHostController** is related to the **SearchServiceInstance**, where the **SearchHostController** manages the search components that run on a server, and maintains a local repository for linguistic dictionaries. The search components retrieve the linguistic dictionaries from the **PrimaryHostController**. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _SearchServiceInstance_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceInstancePipeBind  <br/> |**SearchServiceInstance** of the server from where the **SearchHostController** object is returned.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**SearchServiceInstance** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceInstancePipeBind  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchServiceInstance](get-spenterprisesearchserviceinstance.md)

