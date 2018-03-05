---
title: "Get-SPServiceInstance"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14bbe36e-c73c-428a-955c-2c1e4d8a1d83

description: "Returns the services instance for a specific server or the entire farm."
---

# Get-SPServiceInstance

Returns the services instance for a specific server or the entire farm.
  
```
Get-SPServiceInstance [[-Identity] <SPServiceInstancePipeBind>] [-All <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Get-SPServiceInstance** cmdlet returns the services instance specified by the **Identity** parameter for a specific server. If the **Server** parameter is not specified, the **Get-SPServiceInstance** cmdlet returns results for the entire farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceInstancePipeBind  <br/> |Specifies the GUID of the service instance.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
|**Server** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServerPipeBind  <br/> |Specifies the server from which to return the service instance.  <br/> |
|**All** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Returns all services instance in the farm.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceInstancePipeBind  <br/> ||
|**Server** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServerPipeBind  <br/> ||
|**All** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Get-SPServiceInstance -Server ServerA
```

This example displays the service instances from a given server.
  
## See also

#### 

[Start-SPServiceInstance](start-spserviceinstance.md)
  
[Stop-SPServiceInstance](stop-spserviceinstance.md)

