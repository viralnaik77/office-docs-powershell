---
title: "Get-SPTopologyServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4889f1ac-5f82-4887-919f-8c3cdb6b53ab

description: "Retrieves the topology service application proxy."
---

# Get-SPTopologyServiceApplicationProxy

Retrieves the topology service application proxy.
  
```
Get-SPTopologyServiceApplicationProxy [[-Identity] <SPTopologyWebServiceProxyPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPTopologyServiceApplicationProxy** cmdlet retrieves the local topology service application proxy. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTopologyWebServiceProxyPipeBind  <br/> |Specifies the GUID of the application proxy.  <br/> The type must be a valid GUID, in the form 1234-4567-098jhj.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTopologyWebServiceProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Get-SPTopologyServiceApplicationProxy
```

This example displays the topology service application proxy in the farm. 
  
## See also

#### 

[Set-SPTopologyServiceApplicationProxy](set-sptopologyserviceapplicationproxy.md)
  
[Set-SPTopologyServiceApplication](set-sptopologyserviceapplication.md)

