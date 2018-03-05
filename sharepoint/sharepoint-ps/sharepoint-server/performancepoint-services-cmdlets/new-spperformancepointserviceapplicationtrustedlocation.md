---
title: "New-SPPerformancePointServiceApplicationTrustedLocation"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 48120d61-4011-414a-afb0-5fcb6a840ebe

description: "Creates a new trusted location for a PerformancePoint Service application."
---

# New-SPPerformancePointServiceApplicationTrustedLocation

Creates a new trusted location for a PerformancePoint Service application.
  
```
New-SPPerformancePointServiceApplicationTrustedLocation -ServiceApplication <SPPerformancePointMonitoringServiceApplicationPipeBind> -TrustedLocationType <DataSource | Content> -Type <SiteCollection | Site | List | DocumentLibrary> -Url <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Description <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **New-SPPerformancePointServiceApplicationTrustedLocation** cmdlet creates a new trusted location for a PerformancePoint Service application. The new trusted location can be a **Content** or **Data Source** trusted location type and is enforced only when it is enabled in the PerformancePoint Service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.PerformancePoint.Scorecards.SPPerformancePointMonitoringServiceApplicationPipeBind  <br/> |Specifies the PerformancePoint Service application to which the new trusted location will be added.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a PerformancePoint Service application (for example, PerfPointApp1); or an instance of a valid **SPPerformancePointMonitoringServiceApplication** object.  <br/> |
|**TrustedLocationType** <br/> |Required  <br/> |Microsoft.PerformancePoint.Scorecards.TrustedFileType  <br/> |Specifies the type of trusted locations to create. If **TrustedLocationType** is not specified, this cmdlet creates all the trusted locations for the specified PerformancePoint Service application.  <br/> The type must be one of the following: **Content** or **Data Source**.  <br/> |
|**Type** <br/> |Required  <br/> |Microsoft.PerformancePoint.Scorecards.RepositoryLocationType  <br/> |Specifies the type of trusted location.  <br/> The type must be one of the following: **Site Collection**, **Site**, **Document Library**, **List** <br/> |
|**Url** <br/> |Required  <br/> |System.String  <br/> |Specifies the URL of the trusted location site, site collection, site, document library, or list. The type must be a valid URL, in the form http://server_name, or http://server_name/sitecollection/site/list.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Description** <br/> |Optional  <br/> |System.String  <br/> |Specifies the description of the new safe data provider.  <br/> The type must be a valid string with a maximum of 4096 characters.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.PerformancePoint.Scorecards.SPPerformancePointMonitoringServiceApplicationPipeBind  <br/> ||
|**TrustedLocationType** <br/> |Required  <br/> |Microsoft.PerformancePoint.Scorecards.TrustedFileType  <br/> ||
|**Type** <br/> |Required  <br/> |Microsoft.PerformancePoint.Scorecards.RepositoryLocationType  <br/> ||
|**Url** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Description** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE---------------------
  
```
New-SPPerformancePointServiceApplicationTrustedLocation -ServiceApplication PPSApp_01 -url "http://Some_Valid_Site_URL" -Type Site -TrustedLocationType Content
```

This example creates a new  `TrustedLocation` for the  `PPSApp_01` service application. This creates a  `Content` trusted location of type  `Site` with the specified URL. 
  
## See also

#### 

[Clear-SPPerformancePointServiceApplicationTrustedLocation](clear-spperformancepointserviceapplicationtrustedlocation.md)
  
[Get-SPPerformancePointServiceApplicationTrustedLocation](get-spperformancepointserviceapplicationtrustedlocation.md)
  
[Remove-SPPerformancePointServiceApplicationTrustedLocation](remove-spperformancepointserviceapplicationtrustedlocation.md)

