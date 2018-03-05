---
title: "Update-SPDistributedCacheSize"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8e483d89-60a9-48b8-a2e3-2e848159833b

description: "Reconfigures the allocation of memory that is dedicated to the Distributed Cache service."
---

# Update-SPDistributedCacheSize

Reconfigures the allocation of memory that is dedicated to the Distributed Cache service.
  
```
Update-SPDistributedCacheSize [-CacheSizeInMB] <UInt32> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Update-SPDistributedCacheSize** cmdlet to allocate memory to the Distributed cache service. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**CacheSizeInMB** <br/> |Required  <br/> |System.UInt32  <br/> |Specifies the memory size in megabytes (MB) that you want to allocate to the Distributed Cache service. The default value is 5 percent of total system random access memory (RAM). This value should not be more than 40 percent of total system RAM with a maximum limit of 16 gigabytes (GB).  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**CacheSizeInMB** <br/> |Required  <br/> |System.UInt32  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-------------EXAMPLE---------- 
  
```
Update-SPDistributedCacheSize -CacheSizeInMB 2048
```


