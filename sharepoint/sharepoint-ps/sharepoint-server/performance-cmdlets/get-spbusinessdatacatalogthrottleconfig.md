---
title: "Get-SPBusinessDataCatalogThrottleConfig"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8e81ff1-ee48-4b0c-93b6-933a06655e05

description: "Returns the throttling configuration for a Business Data Connectivity Service application."
---

# Get-SPBusinessDataCatalogThrottleConfig

Returns the throttling configuration for a Business Data Connectivity Service application.
  
```
Get-SPBusinessDataCatalogThrottleConfig -Scope <Global | Database | WebService | Wcf | Custom | OData> -ServiceApplicationProxy <SPServiceApplicationProxyPipeBind> -ThrottleType <None | Items | Size | Connections | Timeout | MetadataSize | ModelSize | MaxNumberOfModels> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Get-SPBusinessDataCatalogThrottleConfig** cmdlet reads the throttling configuration for a Business Data Connectivity Service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**FileBacked** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Requests the throttling configuration for file backed metadata catalogs.  <br/> |
|**Scope** <br/> |Required  <br/> |Microsoft.BusinessData.SystemSpecific.ThrottleScope  <br/> |Returns the throttling configuration for the specified the scope.  <br/> The type must be one of the following: **Global**, **Database**, **WebService**, **Wcf**, or **Custom**.  <br/> |
|**ServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the Business Data Connectivity Service application proxy that contains the throttling configuration to get.  <br/> |
|**ThrottleType** <br/> |Required  <br/> |Microsoft.BusinessData.SystemSpecific.ThrottleType  <br/> |Returns the throttling configuration for the specified throttle type.  <br/> The type must be one of the following: **None**, **Items**, **Size**, **Connections**, or **Timeout**.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**FileBacked** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Scope** <br/> |Required  <br/> |Microsoft.BusinessData.SystemSpecific.ThrottleScope  <br/> ||
|**ServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> ||
|**ThrottleType** <br/> |Required  <br/> |Microsoft.BusinessData.SystemSpecific.ThrottleType  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$contosoServAppProxy  = Get-SPServiceApplicationProxy -Identity <GUID>
 Get-SPBusinessDataCatalogThrottleConfig -Scope Database -ThrottleType Items -ServiceApplicationProxy $contosoServAppProxy
```

This example returns the throttling information that is related to database items for the given service application. You must replace  _\<GUID\>_ with the ID of the ServiceApplicationProxy. 
  
## See also

#### 

[Set-SPBusinessDataCatalogThrottleConfig](set-spbusinessdatacatalogthrottleconfig.md)

