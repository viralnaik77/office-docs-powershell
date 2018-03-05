---
title: "Start-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 362fe4d2-417d-4c5d-9a9f-046580980182

description: "Starts an instance of a search manager service."
---

# Start-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance

Starts an instance of a search manager service.
  
```
Start-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance -Identity <SearchQueryAndSiteSettingsServiceInstancePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$qssInstance = Get-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance -LocalStart-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance -Identity $qssInstance
```

This example starts the local query and site settings instance.
  
## Detailed Description

The **Start-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance** cmdlet starts the query and site settings service instance on the server instance in the same farm as the search service application to host the query object model (OM), Windows Communication Foundation (WCF) endpoint, and query processor for the search service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchQueryAndSiteSettingsServiceInstancePipeBind  <br/> |Specifies the search manager service instance to start.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid SPServer name, or the name of a search manager service instance (for example, SearchManagerServiceInstance1); or an instance of a valid **SearchManagerServiceInstance** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchQueryAndSiteSettingsServiceInstancePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   

