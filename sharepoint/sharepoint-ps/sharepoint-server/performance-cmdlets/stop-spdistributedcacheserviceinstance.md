---
title: "Stop-SPDistributedCacheServiceInstance"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 464d8e79-312f-4e3c-9453-48a3aac5db05

description: "Stops an instance of the distributed cache service on a local server."
---

# Stop-SPDistributedCacheServiceInstance

Stops an instance of the distributed cache service on a local server.
  
```
Stop-SPDistributedCacheServiceInstance [[-Graceful] <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Stop-SPDistributedCacheServiceInstance** cmdlet to stop an instance of the distributed cache service on a local server. 
  
Execution of this cmdlet moves cached items to another server to preserve them. If you stop the distributed service before you stop each instance, cached items are lost. To prevent cached items from being lost, use the **Graceful** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Graceful** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether to gracefully stop an instance of the distributed cache service.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Graceful** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------EXAMPLE---------- 
  
```
Stop-SPDistributedCacheServiceInstance -Graceful
```

This example gracefully stops an instance of a distributed cache service on a local server.
  
## See also

#### 

[Remove-SPDistributedCacheServiceInstanceOnLocalServer](http://technet.microsoft.com/library/d4d1a1f8-eab5-4ae2-8aa0-f25ee807a505.aspx)
  
[Add-SPDistributedCacheServiceInstanceOnLocalServer](http://technet.microsoft.com/library/28c64abc-fdf8-4353-ac9f-05e9ad8e509d.aspx)

