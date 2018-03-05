---
title: "Import-SPSiteSubscriptionBusinessDataCatalogConfig"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fe7698fc-9743-4717-af88-82608160cc1e

description: "Imports data associated with an exported file that contains all data associated with the Business Data Connectivity Metadata Store for a given partition."
---

# Import-SPSiteSubscriptionBusinessDataCatalogConfig

Imports data associated with an exported file that contains all data associated with the Business Data Connectivity Metadata Store for a given partition.
  
```
Import-SPSiteSubscriptionBusinessDataCatalogConfig -Path <String> -ServiceContext <SPServiceContextPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-LocalizedNamesIncluded <SwitchParameter>] [-ModelsIncluded <SwitchParameter>] [-PermissionsIncluded <SwitchParameter>] [-PropertiesIncluded <SwitchParameter>] [-ProxiesIncluded <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Import-SPSiteSubscriptionBusinessDataCatalogConfig** cmdlet to import a data file that contains Business Data Connecitivity models and all data associated with the Business Data Connectivity Metadata Store for a given partition. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies the path and name to use to create the export file.The type must be a valid path in either of the following forms:  <br/> C:\folder_name  <br/> \\server_name\folder_name  <br/> ..\folder_name\file.xml  <br/> |
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context of the data to be exported.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a service context (for example, http://ServiceContext1); or an instance of a valid **SPServiceContext** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**LocalizedNamesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that names for business data fields in multiple languages be imported.  <br/> |
|**ModelsIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that Business Data Connectivity models be included in the imported file.  <br/> |
|**PermissionsIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that permissions from the Business Data Connectivity model be exported.  <br/> |
|**PropertiesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that properties from the Business Data Connectivity model be imported.  <br/> |
|**ProxiesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that proxies for Business Data Connectivity Service Applications be exported.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**LocalizedNamesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ModelsIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**PermissionsIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**PropertiesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ProxiesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------------EXAMPLE--------------------------- 
  
```
Import-SPSiteSubscriptionBusinessDataCatalogConfig -Path "C:\folder\importFile.xml" -ServiceContext http://contoso
```

This example imports the data file named **importFile.xml**.
  
## See also

#### 

[Clear-SPSiteSubscriptionBusinessDataCatalogConfig](clear-spsitesubscriptionbusinessdatacatalogconfig.md)
  
[Export-SPSiteSubscriptionBusinessDataCatalogConfig](export-spsitesubscriptionbusinessdatacatalogconfig.md)
  
[Remove-SPSiteSubscriptionBusinessDataCatalogConfig](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/service-application-cmdlets/remove-spsitesubscriptionbusinessdatacatalogconfig.md)

