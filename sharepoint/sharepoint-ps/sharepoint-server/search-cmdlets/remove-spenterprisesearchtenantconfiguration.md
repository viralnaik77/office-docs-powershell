---
title: "Remove-SPEnterpriseSearchTenantConfiguration"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b2bd659f-3f34-4be2-92f6-1beba3ffefaa

description: "Removes all tenant specific search settings."
---

# Remove-SPEnterpriseSearchTenantConfiguration

Removes all tenant specific search settings.
  
```
Remove-SPEnterpriseSearchTenantConfiguration -SearchApplication <SearchServiceApplicationPipeBind> -SiteSubscriptionId <Guid> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

--------EXAMPLE--------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
```

```
Remove-SPEnterpriseSearchTenantConfiguration -SiteSubscriptionId "00000000-0000-0000-0000-000000000001" -SearchApplication $ssa
```

This example uses **Remove-SPEnterpriseSearchTenantConfiguration** to remove all tenant specific settings from the search service application referenced by **$ssa**. 
  
## Detailed Description

The **Remove-SPEnterpriseSearchTenantConfiguration** cmdlet removes all tenant specific search settings. The removed settings are: query Rules, result types, result sources, managed metadata, ranking models, search dictionaries, authoritative pages, query suggestion settings, client types, and the default search center. Use this cmdlet when removing tenants and in conjunction with moving tenants. When moving a tenant, copy the tenant configuration from the source to the destination, and then use this cmdlet to remove the tenant configuration from the source farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the name of the search application that contains the tenant configuration. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _SiteSubscriptionId_ <br/> |Required  <br/> |System.Guid  <br/> |Specifies the site subscription of the tenant. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SiteSubscriptionId** <br/> |Required  <br/> |System.Guid  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   

