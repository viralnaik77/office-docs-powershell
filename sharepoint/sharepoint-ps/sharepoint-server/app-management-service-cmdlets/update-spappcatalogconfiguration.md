---
title: "Update-SPAppCatalogConfiguration"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ba3d6a8f-db1c-4af7-af96-5ce3ab84cbd9

description: "Sets a specific site collection as the App Catalog site collection."
---

# Update-SPAppCatalogConfiguration

Sets a specific site collection as the App Catalog site collection.
  
```
Update-SPAppCatalogConfiguration [-Site] <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-SkipWebTemplateChecking <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Update-SPAppCatalogConfiguration** cmdlet to set a specific site collection as the App Catalog site collection. The App Catalog site collection contains catalogs for Apps for SharePoint and Apps for Office. It is used to help ITPro administrators distribute SharePoint Apps and Office Apps to their end users. Each Web Application or Tenancy can have 1 App Catalog Site collection associated to it. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the URL or GUID of the site collection to be set as the app catalog site collection.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to force marking the site collection even if there are validation errors.  <br/> |
|**SkipWebTemplateChecking** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether to skip checking if the template of the site is **APCATALOG#0** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SkipWebTemplateChecking** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------EXAMPLE----------- 
  
```
Update-SPAppCatalogConfiguration -Site http://localhost/sites/appcatalog_1 -Force:$true -SkipWebTemplateChecking:$true
```

This example sets http://localhost/sites/appcatalog_1 as the app catalog site collection for the tenant it belongs to.
  

