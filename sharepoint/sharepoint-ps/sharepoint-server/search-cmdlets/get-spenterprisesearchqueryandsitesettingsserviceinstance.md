---
title: "Get-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f1438a74-92fb-498d-aac1-66743403f3bc

description: "Returns the service manager service instance."
---

# Get-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance

Returns the service manager service instance.
  
```
Get-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance [-AssignmentCollection <SPAssignmentCollection>] [-Identity <SearchQueryAndSiteSettingsServiceInstancePipeBind>] [-Local <SwitchParameter>]

```

## Example

------------------EXAMPLE 1------------------
  
```
$qqssSvcInstance = Get-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance -Local
```

This example obtain a reference to the query and site setting service instance on the local farm.
  
------------------EXAMPLE 2------------------
  
```
$qssSvcInstance = Get-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance -Identity myServer
```

This example obtain a reference to the query and site setting service instance from a specific server name.
  
## Detailed Description

The **Get-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance** cmdlet returns the service manager service instance when a search manager service is started or stopped. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchQueryAndSiteSettingsServiceInstancePipeBind  <br/> |Specifies the search manager service instance to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid server name on which search manager service instance runs; or an instance of a valid **SearchManagerServiceInstance** object.  <br/> |
| _Local_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the service manager service instance for the current search server is returned.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchQueryAndSiteSettingsServiceInstancePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Local** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   

