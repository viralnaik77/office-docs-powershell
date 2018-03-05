---
title: "Set-SPPowerPointConversionServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6eb45c62-4261-4cc1-8de2-2753d13aaeab

description: "Configures settings for a PowerPoint Conversion Service application."
---

# Set-SPPowerPointConversionServiceApplication

Configures settings for a PowerPoint Conversion Service application. 
  
```
Set-SPPowerPointConversionServiceApplication [-Identity] <SPPowerPointConversionServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-CacheExpirationPeriodInSeconds <UInt32>] [-MaximumConversionsPerWorker <UInt32>] [-WorkerKeepAliveTimeoutInSeconds <UInt32>] [-WorkerProcessCount <UInt32>] [-WorkerTimeoutInSeconds <UInt32>]
```

## Detailed Description

Use the **Set-SPPowerPointConversionServiceApplication** cmdlet to set properties and settings for an instance of a PowerPoint Conversion Service application that is in a farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.PowerPoint.PowerShell.SPPowerPointConversionServiceApplicationPipeBind  <br/> |Specifies the unique name of this PowerPoint Conversion Service application.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CacheExpirationPeriodInSeconds** <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the maximum time, in seconds, that items remain in the back-end server cache. The default value is 600 seconds (10 minutes).  <br/> |
|**MaximumConversionsPerWorker** <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the maximum number of presentations that a conversion worker process can convert before recycling. The default value is 5.  <br/> |
|**WorkerKeepAliveTimeoutInSeconds** <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the maximum time, in seconds, that a conversion worker process can be unresponsive before being terminated. The default value is 120 seconds.  <br/> |
|**WorkerProcessCount** <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the number of active instances of the conversion worker process on each back-end. This value must be less than the Windows Communication Foundation (WCF) connection limit for this computer. The default value is 3.  <br/> |
|**WorkerTimeoutInSeconds** <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the maximum time, in seconds, that a conversion worker process is given for any single conversion. The default is 300 seconds (5 minutes).  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.PowerPoint.PowerShell.SPPowerPointConversionServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CacheExpirationPeriodInSeconds** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**MaximumConversionsPerWorker** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**WorkerKeepAliveTimeoutInSeconds** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**WorkerProcessCount** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**WorkerTimeoutInSeconds** <br/> |Optional  <br/> |System.UInt32  <br/> ||
   
## Example

-----------EXAMPLE 1------- 
  
```
Set-SPPowerPointConversionServiceApplication -Identity "MyWorkgroupPPTApp" -CacheExpirationPeriodInSeconds 1200
```

This example establishes new operational defaults for the conversion cache expiration.
  
-----------EXAMPLE 2------- 
  
```
Set-SPPowerPointConversionServiceApplication -Identity "MyWorkgroupPPTApp" -DisableBinaryScan:$false
```

This example disables binary scanning of documents.
  
## See also

#### 

[New-SPPowerPointConversionServiceApplication](new-sppowerpointconversionserviceapplication.md)
  
[New-SPPowerPointConversionServiceApplicationProxy](new-sppowerpointconversionserviceapplicationproxy.md)

