---
title: "Get-SPServiceApplicationProxyGroup"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c1d0002-69e2-44fb-b56a-8df8a9e56fa4

description: "Returns the proxy group for the specified service application."
---

# Get-SPServiceApplicationProxyGroup

Returns the proxy group for the specified service application.
  
```
Get-SPServiceApplicationProxyGroup [[-Identity] <SPServiceApplicationProxyGroupPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPServiceApplicationProxyGroup** cmdlet displays a list of the proxy groups in the farm. To display a specific proxy group, use the **Identity** parameter. If no parameter value is specified, a list of all proxy groups is displayed. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyGroupPipeBind  <br/> |Specifies the name or the GUID of the proxy group.  <br/> |
|**Default** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Returns the default sevice proxy group for the farm.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyGroupPipeBind  <br/> ||
|**Default** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Get-SPServiceApplicationProxyGroup
```

This example retrieves all of the service application proxy groups in the farm.
  
## See also

#### 

[New-SPServiceApplicationProxyGroup](new-spserviceapplicationproxygroup.md)
  
[Remove-SPServiceApplicationProxyGroup](remove-spserviceapplicationproxygroup.md)
  
[Add-SPServiceApplicationProxyGroupMember](add-spserviceapplicationproxygroupmember.md)

