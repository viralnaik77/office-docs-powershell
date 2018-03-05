---
title: "Remove-SPDistributedCacheServiceInstance"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7cb14284-d0d8-4221-b81d-0a4470101880

description: "Removes an instance of the distributed cache service from a local server."
---

# Remove-SPDistributedCacheServiceInstance

Removes an instance of the distributed cache service from a local server.
  
```
Remove-SPDistributedCacheServiceInstance [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Remove-SPDistributedCacheServiceInstance** cmdlet to remove an instance of the distributed cache service from a local server. This is required to stop the AppFabric service. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------EXAMPLE---- 
  
```
Remove-SPDistributedCacheServiceInstance
```

This example removes an instance of a distributed cache.
  
## See also

#### 

[Stop-SPDistributedCacheServiceInstance](stop-spdistributedcacheserviceinstance.md)
#### 

[Add-SPDistributedCacheServiceInstance](add-spdistributedcacheserviceinstance.md)

