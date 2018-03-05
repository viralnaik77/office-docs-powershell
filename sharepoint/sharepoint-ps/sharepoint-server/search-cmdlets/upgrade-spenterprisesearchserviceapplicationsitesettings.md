---
title: "Upgrade-SPEnterpriseSearchServiceApplicationSiteSettings"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 2/11/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2cbb3074-6327-4fd7-ab14-b6b22baab6f2

description: "The Upgrade-SPEnterpriseSearchServiceApplicationSiteSettings cmdlet has been deprecated and will be removed in a future release."
---

# Upgrade-SPEnterpriseSearchServiceApplicationSiteSettings

The **Upgrade-SPEnterpriseSearchServiceApplicationSiteSettings** cmdlet has been deprecated and will be removed in a future release. 
  
Upgrades search settings for a particular site collection.
  
```
Upgrade-SPEnterpriseSearchServiceApplicationSiteSettings -Identity <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

--------EXAMPLE--------
  
```
$site= Get-SPSite http://test
Upgrade-SPEnterpriseSearchServiceApplicationSiteSettings -Identity $site
```

This example upgrades the search settings for the site collection referenced by  `$site`.
  
## Detailed Description

Use the **Upgrade-SPEnterpriseSearchServiceApplicationSiteSettings** cmdlet to upgrade the search settings for specified site collection from 2010 to 2013 experience. The upgrades include conversion of best bets to query rules. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the site collection for which to upgrade search settings. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Remove-SPEnterpriseSearchServiceApplicationSiteSettings](remove-spenterprisesearchserviceapplicationsitesettings.md)

