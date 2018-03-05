---
title: "Get-SPAppStoreWebServiceConfiguration"
ms.author: kirks
author: Techwriter40
ms.date: 11/20/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e044ee6-9265-4fa2-a731-1eecc1052d01

description: "Returns properties of a SharePoint Store app."
---

# Get-SPAppStoreWebServiceConfiguration

Returns properties of a SharePoint Store app.
  
```
Get-SPAppStoreWebServiceConfiguration [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

------------EXAMPLE-------
  
```
Get-SPAppStoreWebServiceConfiguration
```

This example returns the product type and version for a SharePoint Store app.
  
## Detailed Description

Use the **Get-SPAppStoreWebServiceConfiguration** cmdlet to return property settings (On-premises or Online) for SharePoint Store apps. 
  
> [!NOTE]
> This cmdlet is not intended for the ITPro audience. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## See also

#### 

[Set-SPAppStoreWebServiceConfiguration](set-spappstorewebserviceconfiguration.md)

