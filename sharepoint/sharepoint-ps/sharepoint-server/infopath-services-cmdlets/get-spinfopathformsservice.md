---
title: "Get-SPInfoPathFormsService"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 334e1eba-49eb-4b4a-9850-74b304e8a403

description: "Returns the InfoPath Forms Services in SharePoint Server 2013 settings that are in the farm."
---

# Get-SPInfoPathFormsService

Returns the InfoPath Forms Services in SharePoint Server 2013 settings that are in the farm.
  
```
Get-SPInfoPathFormsService [-AssignmentCollection <SPAssignmentCollection>] [-Identity <SPFormsServicePipeBind>]
```

## Detailed Description

The **Get-SPInfoPathFormsService** cmdlet reads the settings for the InfoPath Forms Services in SharePoint Server 2013. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPFormsServicePipeBind  <br/> |Specifies the InfoPath Forms Services settings to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a forms service (for example, FormsService1); or an instance of a valid **SPFormsService** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPFormsServicePipeBind  <br/> ||
   
## Example

-----------EXAMPLE----------------
  
```
Get-SPInfoPathFormsService
```

This example displays the InfoPath Forms Services settings for the entire farm.
  
## See also

#### 

[Set-SPInfoPathFormsService](set-spinfopathformsservice.md)

