---
title: "Get-SPAccessServicesApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e237234-6d29-4e34-a5aa-2a4dc951cc1e

description: "Returns an Access Services application or a collection of Access Services applications."
---

# Get-SPAccessServicesApplication

Returns an Access Services application or a collection of Access Services applications.
  
```
Get-SPAccessServicesApplication [[-Identity] <SPServiceApplicationPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPAccessServiceApplication** cmdlet retrieves an Access Services application. If an identity is not specified, the cmdlet returns the collection of Access Services applications that are in the farm. The properties returned from this cmdlet are read-only. To update properties of a Access Services application, use the **Set-SPAccessServiceApplication** cmdlet. Updates affect all servers in the farm in which this Access Services application runs. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> |Specifies the Access Services application to return.  <br/> The value must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid **SPAccessServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------EXAMPLE 1----------------
  
```
Get-SPAccessServiceApplication -Identity "MyAccessService"
```

This example returns an Access Services application named  `MyAccessService`.
  
------------EXAMPLE 2----------------
  
```
Get-SPAccessServiceApplication
```

This example returns every Access Services application in the farm.
  
## See also

#### 

[New-SPAccessServicesApplication](new-spaccessservicesapplication.md)
  
[Set-SPAccessServicesApplication](set-spaccessservicesapplication.md)

