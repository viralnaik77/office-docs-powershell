---
title: "Get-SPEnterpriseSearchServiceApplicationProxy"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 233890cc-6571-4bd3-bb59-2b549a6098c3

description: "Returns the search service application proxy."
---

# Get-SPEnterpriseSearchServiceApplicationProxy

Returns the search service application proxy.
  
```
Get-SPEnterpriseSearchServiceApplicationProxy [-AssignmentCollection <SPAssignmentCollection>] [-Identity <SearchServiceApplicationProxyPipeBind>]

```

## Example

------------------EXAMPLE------------------
  
```
$ssaProxy = Get-SPEnterpriseSearchServiceApplicationProxy -Identity SsaProxy
```

This example obtains a reference to a search service application proxy with the name  `SsaProxy`.
  
## Detailed Description

This cmdlet reads the **SearchServiceApplicationProxy** object when the search service application proxy is created updated or deleted. If the **Identity** parameter is not specified, this cmdlet returns the search service application proxy collection for the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationProxyPipeBind  <br/> |Specifies the search service application proxy to retrieve.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a search service application proxy (for example, SearchServiceAppProxy1); or an instance of a valid **SearchServiceApplicationProxy** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[Set-SPEnterpriseSearchServiceApplicationProxy](set-spenterprisesearchserviceapplicationproxy.md)
  
[New-SPEnterpriseSearchServiceApplicationProxy](new-spenterprisesearchserviceapplicationproxy.md)
  
[Remove-SPEnterpriseSearchServiceApplicationProxy](remove-spenterprisesearchserviceapplicationproxy.md)

