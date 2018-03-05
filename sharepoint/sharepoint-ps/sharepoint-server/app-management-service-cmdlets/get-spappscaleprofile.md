---
title: "Get-SPAppScaleProfile"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b6e2fe76-53ec-4a88-80a7-6cd27aa80f91

description: "Returns settings for an app profile."
---

# Get-SPAppScaleProfile

Returns settings for an app profile.
  
```
Get-SPAppScaleProfile [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Get-SPAppScaleProfile** cmdlet to return settings for an app profile. 
  
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

---------------EXAMPLE--------------
  
```
$scaleProfile = Get-SPAppScaleProfile
```

```
$scaleProfile.MaxDatabaseSize
```

```
$scaleProfile.RemoteWebSiteInstanceCount
```

This example returns the farm level app scale profile.
  
## See also

#### 

[Set-SPAppScaleProfile](set-spappscaleprofile.md)

