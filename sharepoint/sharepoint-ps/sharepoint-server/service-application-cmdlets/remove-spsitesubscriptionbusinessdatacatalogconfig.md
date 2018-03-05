---
title: "Remove-SPSiteSubscriptionBusinessDataCatalogConfig"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b244a460-1b02-45cf-a21b-780f7c921a87

description: "Removes the Business Data Connectivity Metadata Store for a partition."
---

# Remove-SPSiteSubscriptionBusinessDataCatalogConfig

Removes the Business Data Connectivity Metadata Store for a partition.
  
```
Remove-SPSiteSubscriptionBusinessDataCatalogConfig -ServiceContext <SPServiceContextPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPSiteSubscriptionBusinessDataCatalogConfig** cmdlet removes the Business Data Connectivity Metadata Store and all associated data for a specified partition. To completely remove a partition and the data that it contains, run the **Clear-SPSiteSubscriptionBusinessDataCatalogConfig** cmdlet to remove the data from the Business Data Connectivity Metadata Store, and then run the **Remove-SPSiteSubscriptionBusinessDataCatalogConfig** cmdlet. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context of the Business Data Connectivity Metadata Store to remove.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a service context (for example, http://ServiceContext1); or an instance of a valid **SPServiceContext** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Remove-SPSiteSubscriptionBusinessDataCatalogConfig -ServiceContext http://contoso
```

This example removes the Business Data Connectivity Metadata Store for the partition  `http://contoso`.
  
## See also

#### 

[Export-SPSiteSubscriptionBusinessDataCatalogConfig](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/business-connectivity-services-cmdlets/export-spsitesubscriptionbusinessdatacatalogconfig.md)
  
[Import-SPSiteSubscriptionBusinessDataCatalogConfig](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/business-connectivity-services-cmdlets/import-spsitesubscriptionbusinessdatacatalogconfig.md)

