---
title: "Remove-SPEnterpriseSearchServiceApplicationSiteSettings"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 2/11/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 000b95e2-3198-42e9-a6e4-2398e803e023

description: "The Remove-SPEnterpriseSearchServiceApplicationSiteSettings cmdlet has been deprecated and will be removed in a future release."
---

# Remove-SPEnterpriseSearchServiceApplicationSiteSettings

The **Remove-SPEnterpriseSearchServiceApplicationSiteSettings** cmdlet has been deprecated and will be removed in a future release. 
  
Cleans up search settings for a particular site collection, subscription, or search application.
  
```
Remove-SPEnterpriseSearchServiceApplicationSiteSettings -Identity <SiteSettingsPipeBind> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-TenantId <Guid>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------EXAMPLE--------
  
```
$app = Get-SPEnterpriseSearchServiceApplication
$GC = Start-SPAssignment
$s = $GC | Get-SPSite UrlOfASiteCollection
Remove-SPEnterpriseSearchServiceApplicationSiteSettings -Identity $s.ID.ToString() -SearchApplication $app
Stop-SPAssignment $GC
```

This example removes the search settings for the site collection referenced by **$s** in the search application referenced by **$app**. **$s** is the site collection with URL "UrlOfSiteCollection", and **$s.ID.ToString()** is the string representation of the site ID. 
  
## Detailed Description

Use the **Remove-SPEnterpriseSearchServiceApplicationSiteSettings** cmdlet to remove all search settings for the specified site collection, subscription, or search application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SiteSettingsPipeBind  <br/> |Specifies the site collection to remove search settings from. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the name of the search application. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _TenantId_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies the tenant from which to remove search settings. The type must be a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SiteSettingsPipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**TenantId** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Upgrade-SPEnterpriseSearchServiceApplicationSiteSettings](upgrade-spenterprisesearchserviceapplicationsitesettings.md)

