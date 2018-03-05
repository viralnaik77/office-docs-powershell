---
title: "Get-SPUserLicensing"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 985db4e7-e218-4346-a376-48f825923002

description: "Returns the state of user-license enforcement."
---

# Get-SPUserLicensing

Returns the state of user-license enforcement.
  
```
Get-SPUserLicensing [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPUserLicensing** cmdlet returns the state of user-license enforcement for an entire SharePoint farm. 
  
If user-license enforcement is enabled on a SharePoint farm, the return value is true. Otherwise the value is false.
  
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

---------------EXAMPLE------------- 
  
```
Get-SPUserLicensing
```

This example returns the state of user-license enforcement on the SharePoint farm.
  
## See also

#### 

[Disable-SPUserLicensing](disable-spuserlicensing.md)
  
[Enable-SPUserLicensing](enable-spuserlicensing.md)

