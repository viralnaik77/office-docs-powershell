---
title: "Set-SPVisioPerformance"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6233c2c3-dc40-4436-bc78-f9b9ecb8b62e

description: "Sets performance properties for a Visio Services application."
---

# Set-SPVisioPerformance

Sets performance properties for a Visio Services application.
  
```
Set-SPVisioPerformance -MaxCacheSize <Int64> -MaxDiagramCacheAge <Int32> -MaxDiagramSize <Int64> -MaxRecalcDuration <Int32> -MinDiagramCacheAge <Int32> -VisioServiceApplication <SPVisioServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

-------------------EXAMPLE 1----------------------
  
```
Set-SPVisioPerformance -VisioServiceApplication "VGS2" -MaxDiagramSize 10 -MaxRecalcDuration 120 -MinDiagramCacheAge 1 -MaxDiagramCacheAge 4
```

This example changes settings that are related to performance for a Visio Services application.
  
-------------------EXAMPLE 2----------------------
  
```
Set-SPVisioPerformance -VisioServiceApplication "VGS2" -MaxDiagramSize 10
```

This example changes settings that are related to performance for a Visio Services application. Note that only one setting value is specified. The cmdlet prompts you for the other parameter values.
  
## Detailed Description

The **Set-SPVisioPerformance** cmdlet sets properties related to performance for a Visio Services application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _MaxCacheSize_ <br/> |Required  <br/> |System.Int64  <br/> |PARAMVALUE: Int64  <br/> |
| _MaxDiagramCacheAge_ <br/> |Required  <br/> |System.Int32  <br/> |Specifies the time, in minutes, after which cached items are purged. This value affects memory use on the server. A large cache age slows the rate at which diagrams can be refreshed by users and reduces CPU and memory use of the server. The default value is 60 minutes.  <br/> The type must be an integer in the range of 0 to 34560 (24 days).  <br/> |
| _MaxDiagramSize_ <br/> |Required  <br/> |System.Int64  <br/> |Specifies the maximum size, in megabytes, of a diagram that can be opened by the Visio Services application. The default value is **5**.  <br/> The type must be an integer in the range of 1 to 50.  <br/> |
| _MaxRecalcDuration_ <br/> |Required  <br/> |System.Int32  <br/> |Specifies the maximum time, in seconds, that a diagram can only be recalculated by the Visio Services application. Diagram recalculation operations that take longer than this number of seconds are canceled by the service. A low value increases performance by allowing only simple diagrams to be processed by the server, which minimizes CPU and memory use. A larger value allows the recalculation of more complex diagrams while using more CPU cycles and memory.  <br/> The type must be a valid integer value in the range of 1 to 120 seconds (2 minutes). The default value is 60 seconds.  <br/> |
| _MinDiagramCacheAge_ <br/> |Required  <br/> |System.Int32  <br/> |Specifies the minimum time, in minutes, a diagram is cached in memory. This value affects memory use on the server. A small value allows users to refresh their diagrams more often, but will increase memory and CPU load of the server. The default value is **5**.  <br/> The type must be an integer in the range of 0 to 34560 (24 days).  <br/> |
| _VisioServiceApplication_ <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> |Specifies the Visio Services application that contains the **SPVisioPerformance** object.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a Visio Services application (for example, MyVisioService1); or an instance of a valid **SPVisioServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Maximum Caches Size** <br/> |Required  <br/> |System.Int32  <br/> |The maximum cache size in MB (between 100 and 1024000) that can be used. A larger size limit may lead to more disk resource usage by the service, while a smaller limit may impact performance.Valid values range from 100 to 1024000. The default value is 5120 MB.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Maximum Cache Size** <br/> |Required  <br/> |System.Int32  <br/> ||
|**MaxDiagramCacheAge** <br/> |Required  <br/> |System.Int32  <br/> ||
|**MaxDiagramSize** <br/> |Required  <br/> |System.Int64  <br/> ||
|**MaxRecalcDuration** <br/> |Required  <br/> |System.Int32  <br/> ||
|**MinDiagramCacheAge** <br/> |Required  <br/> |System.Int32  <br/> ||
|**VisioServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[Get-SPVisioPerformance](get-spvisioperformance.md)

