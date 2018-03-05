---
title: "Get-SPTopologyServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fc40e2b8-5710-4034-b37f-b4e61008410a

description: "Displays properties of the topology service application for the current farm."
---

# Get-SPTopologyServiceApplication

Displays properties of the topology service application for the current farm.
  
```
Get-SPTopologyServiceApplication [[-Identity] <SPTopologyWebServiceApplicationPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPTopologyServiceApplication** cmdlet displays the advanced properties of an application when the **Identity** parameter is used. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTopologyWebServiceApplicationPipeBind  <br/> |Specifies the GUID of the application.  <br/> The type must be a valid GUID, in the form 1234-4567-098jhj.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTopologyWebServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Get-SPTopologyServiceApplication
```

This example displays properties of the topology service application for the current farm.
  
## See also

#### 

[Set-SPTopologyServiceApplication](set-sptopologyserviceapplication.md)
  
[Get-SPTopologyServiceApplicationProxy](get-sptopologyserviceapplicationproxy.md)

