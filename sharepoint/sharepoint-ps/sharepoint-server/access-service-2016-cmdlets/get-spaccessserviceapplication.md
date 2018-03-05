---
title: "Get-SPAccessServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c3c2bbc-553c-4782-a567-006fd458d9d5

description: "Returns an Access Services application or a collection of Access Services applications."
---

# Get-SPAccessServiceApplication

Returns an Access Services application or a collection of Access Services applications.
  
```
Get-SPAccessServiceApplication [[-Identity] <SPAccessServiceApplicationPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPAccessServiceApplication** cmdlet retrieves an Access Services application. If an identity is not specified, the cmdlet returns the collection of Access Services applications that are in the farm. The properties returned from this cmdlet are read-only. If changes need to be made, use the **Set-SPAccessServiceApplication** cmdlet. These changes affect all computers in the farm in which this Access Services application runs. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Access.Server.PowerShell.SPAccessServiceApplicationPipeBind  <br/> |Specifies the Access Services application to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid **SPAccessServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Access.Server.PowerShell.SPAccessServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------EXAMPLE 1----------------
  
```
Get-SPAccessServiceApplication -identity "MyAccessService"
```

This example displays an Access Services application named  `MyAccessService`.
  
------------EXAMPLE 2----------------
  
```
Get-SPAccessServiceApplication | where {$_.recordsintablemax -gt 10000}
```

This example displays every Access Services application that run in the farm, which allows more than 10,000 records in a table.
  
------------EXAMPLE 3----------------
  
```
Get-SPAccessServiceApplication
```

This example displays every Access Services application in the farm.
  
## See also

#### 

[Set-SPAccessServiceApplication](set-spaccessserviceapplication.md)

