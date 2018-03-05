---
title: "Get-SPVisioServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a9d3c208-c14f-4937-bdd5-65ca551f453a

description: "Returns properties of a Visio Services application proxy or a collection of Visio Services application proxies."
---

# Get-SPVisioServiceApplicationProxy

Returns properties of a Visio Services application proxy or a collection of Visio Services application proxies.
  
```
Get-SPVisioServiceApplicationProxy [[-Identity] <SPVisioServiceApplicationProxyPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPVisioServiceApplicationProxy** cmdlet reads the settings of a Visio Services application proxy. If the **Identity** parameter is not specified, this cmdlet returns the collection of Visio Services application proxies on the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationProxyPipeBind  <br/> |Specifies the Visio Services application proxy to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a Visio Services application (for example, MyVisioService1); or an instance of a valid **SPVisioServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

----------------EXAMPLE 1---------------------
  
```
Get-SPVisioServiceApplicationProxy
```

This example returns a list of Visio Services application proxies.
  
----------------EXAMPLE 2---------------------
  
```
Get-SPVisioServiceApplicationProxy "Connection to VGS2"
```

This example returns settings for a Visio Services application proxy.
  
## See also

#### 

[New-SPVisioServiceApplicationProxy](new-spvisioserviceapplicationproxy.md)

