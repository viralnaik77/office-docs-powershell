---
title: "Get-SPManagedPath"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e0355fdc-1518-4008-a7cf-10d30d960c5f

description: "Returns all managed paths that match the given criteria."
---

# Get-SPManagedPath

Returns all managed paths that match the given criteria.
  
```
Get-SPManagedPath [[-Identity] <SPPrefixPipeBind>] -WebApplication <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Get-SPManagedPath** cmdlet returns the SharePoint managed path that matches the provided Identity for either a Web application, site collection or for all HostHeader site collections. If an **Identity** parameter is not provided, all managed paths for the given scope are returned. 
  
HostHeader sites (no matter the Web application in which they are contained) share a single set of managed paths. Use the **HostHeader** parameter to return host header managed paths. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPPrefixPipeBind  <br/> |Specifies the URL or GUID of the managed path to return.  <br/> The type must be a valid URL, in the http://server_name or a valid GUID (for example, 12345678-90ab-cdef-1234-567890bcdefgh).  <br/> |
|**HostHeader** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |If provided, the managed paths returned are for the HostHeader sites in the farm.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the URL or GUID of the Web application from which to get the managed path.  <br/> The type must be a valid URL, in the form http://server_name, or a valid GUID (for example, 12345678-90ab-cdef-1234-567890bcdefgh).  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPPrefixPipeBind  <br/> ||
|**HostHeader** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------EXAMPLE 1-----------------
  
```
Get-SPManagedPath -WebApplication http://sitename
```

This example returns all managed paths for the specified Web application.
  
--------------EXAMPLE 2-----------------
  
```
Get-SPManagedPath -identity "Sites" -HostHeader
```

This example gets the  `Sites` managed path from the  `HostHeader` managed paths. 
  
## See also

#### 

[New-SPManagedPath](new-spmanagedpath.md)
  
[Remove-SPManagedPath](remove-spmanagedpath.md)

