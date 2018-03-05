---
title: "Add-SPDistributedCacheServiceInstance"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 9/9/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f4dbede-70a4-4480-9d7a-4265a04c88d1

description: "Adds an instance of the distributed cache service to a local server."
---

# Add-SPDistributedCacheServiceInstance

Adds an instance of the distributed cache service to a local server.
  
```
Add-SPDistributedCacheServiceInstance  <COMMON PARAMETERS>

```

## Example

------------EXAMPLE--------- 
  
```
Add-SPDistributedCacheServiceInstance
```

This example adds an instance of the distributed cache service to a local server.
  
## Detailed Description

Use the **Add-SPDistributedCacheServiceInstance** cmdlet to add an instance of the distributed cache server to a local server. This is required to start the AppFabric service. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CacheSizeInMB_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the amount of RAM to allocate for the Distributed Cache service instance.  <br/> If this parameter is not specified, the default value will be used.  <br/> |
| _Role_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPServerRole  <br/> | Specifies the type of server role that the Distributed Cache service instance should be configured for.  <br/>  This parameter is typically used when you are going to do a server role conversion to the specified server role.  <br/>  The valid values are:  <br/>  SingleServerFarm  <br/>  DistributedCache  <br/>  WebFrontEndWithDistributedCache  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[Stop-SPDistributedCacheServiceInstance](stop-spdistributedcacheserviceinstance.md)
#### 

[Remove-SPDistributedCacheServiceInstance](remove-spdistributedcacheserviceinstance.md)

