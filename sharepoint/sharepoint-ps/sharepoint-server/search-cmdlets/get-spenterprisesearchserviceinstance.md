---
title: "Get-SPEnterpriseSearchServiceInstance"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 309d98e8-a5fa-4cb5-b6e1-bf94380a8212

description: "Returns the search service instance for a farm."
---

# Get-SPEnterpriseSearchServiceInstance

Returns the search service instance for a farm.
  
```
Get-SPEnterpriseSearchServiceInstance [-AssignmentCollection <SPAssignmentCollection>] [-Identity <SearchServiceInstancePipeBind>] [-Local <SwitchParameter>]

```

## Example

------------------EXAMPLE------------------
  
```
$ssInstance = Get-SPEnterpriseSearchServiceInstance -Local
```

This example obtains a reference to the local search service instance.
  
## Detailed Description

This cmdlet returns the **SearchServiceInstance** object when the object is created, updated, or deleted. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceInstancePipeBind  <br/> |Specifies the search service instance to return.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a query server (for example, MyQueryServer); or an instance of a valid **SearchServiceInstance** object.  <br/> |
| _Local_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Returns the search service instance for the current search server.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceInstancePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Local** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Start-SPEnterpriseSearchServiceInstance](start-spenterprisesearchserviceinstance.md)
  
[Stop-SPEnterpriseSearchServiceInstance](stop-spenterprisesearchserviceinstance.md)

