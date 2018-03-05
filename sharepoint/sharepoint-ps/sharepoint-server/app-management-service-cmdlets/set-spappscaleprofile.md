---
title: "Set-SPAppScaleProfile"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/20/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d08f2e3b-2917-4ae5-a422-8b60e37b7901

description: "Sets settings for the app profile."
---

# Set-SPAppScaleProfile

Sets settings for the app profile.
  
```
Set-SPAppScaleProfile [-AssignmentCollection <SPAssignmentCollection>] [-MaxDatabaseSize <String>] [-RemoteWebSiteInstanceCount <Int32>]
```

## Detailed Description

Use the **Set-SPAppScaleProfile** cmdlet to set settings for an app profile. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**MaxDatabaseSize** <br/> |Optional  <br/> |System.String  <br/> |Specifies the database size of the app profile.  <br/> |
|**RemoteWebSiteInstanceCount** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies whether a remote site can access the profile from.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**MaxDatabaseSize** <br/> |Optional  <br/> |System.String  <br/> ||
|**RemoteWebSiteInstanceCount** <br/> |Optional  <br/> |System.Int32  <br/> ||
   
## Example

-----------------EXAMPLE-----------
  
```
Set-SPAppScaleProfile -MaxDatabaseSize "2 GB" -RemoteWebSiteInstanceCount 1
```

This example sets the farm level app scale profile.
  
## See also

#### 

[Get-SPAppScaleProfile](get-spappscaleprofile.md)

