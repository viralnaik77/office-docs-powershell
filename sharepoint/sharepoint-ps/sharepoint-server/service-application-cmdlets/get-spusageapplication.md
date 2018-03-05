---
title: "Get-SPUsageApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04dea0e0-f46c-441f-a0f4-58e432b20575

description: "Returns a specified usage application."
---

# Get-SPUsageApplication

Returns a specified usage application.
  
```
Get-SPUsageApplication [[-Identity] <SPUsageApplicationPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-UsageService <SPUsageServicePipeBind>]
```

## Detailed Description

The **Get-SPUsageApplication** cmdlet return a specified usage application. If the **Identity** parameter is not specified, the cmdlet returns the local usage application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUsageApplicationPipeBind  <br/> |Specifies the usage application to get. If the Identity parameter is not specified, the cmdlet returns the local usage application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a usage application (for example, UsageApplication1); or an instance of a valid **SPUsageApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**UsageService** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUsageServicePipeBind  <br/> |Filters to return the usage application with the specified parent **SPUsageService** object.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a usage service (for example, UsageService1); or an instance of a valid **SPUsageService** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUsageApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**UsageService** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUsageServicePipeBind  <br/> ||
   
## Example

---------------EXAMPLE------------------
  
```
Get-SPUsageApplication -Identity "Usage and Health data collection"
```

This example returns the usage application named,  `Usage and Health data collection`
  
## See also

#### 

[New-SPUsageApplication](new-spusageapplication.md)
  
[Set-SPUsageApplication](set-spusageapplication.md)
  
[Remove-SPUsageApplication](remove-spusageapplication.md)

