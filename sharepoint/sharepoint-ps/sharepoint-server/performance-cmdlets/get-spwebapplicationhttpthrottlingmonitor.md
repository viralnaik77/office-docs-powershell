---
title: "Get-SPWebApplicationHttpThrottlingMonitor"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa927d75-bd9a-40d8-b975-0b0e6577b969

description: "Returns all counters and their associated Health Score bucket values for network throttling on a Web application."
---

# Get-SPWebApplicationHttpThrottlingMonitor

Returns all counters and their associated Health Score bucket values for network throttling on a Web application.
  
```
Get-SPWebApplicationHttpThrottlingMonitor [-Identity] <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPWebApplicationHttpThrottlingMonitor** cmdlet reads all counters for network throttling on a Web application. This cmdlet returns a list that contains all of the performance counters and their associated Health Score bucket values. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Returns throttling performance counter settings for the specified SharePoint Web application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of SharePoint Web application (for example, MyOfficeApp1); or an instance of a valid **SPWebApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$s = get-SPWebApplicationHTTPThrottlingMonitors http://sharepoint 
```

This example gets all performance counters that are being read in the network throttling monitor for the  `http://sharepoint` Web application. 
  
## See also

#### 

[Set-SPWebApplicationHttpThrottlingMonitor](set-spwebapplicationhttpthrottlingmonitor.md)
  
[Enable-SPWebApplicationHttpThrottling](enable-spwebapplicationhttpthrottling.md)
  
[Disable-SPWebApplicationHttpThrottling](disable-spwebapplicationhttpthrottling.md)

