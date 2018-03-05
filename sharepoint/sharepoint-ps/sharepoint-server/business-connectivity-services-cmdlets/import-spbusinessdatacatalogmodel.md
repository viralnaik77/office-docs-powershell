---
title: "Import-SPBusinessDataCatalogModel"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88af66b5-7ebf-4f9e-98fa-1dbb68a2adfc

description: "Imports a Business Data Connectivity Model."
---

# Import-SPBusinessDataCatalogModel

Imports a Business Data Connectivity Model.
  
```
Import-SPBusinessDataCatalogModel -Identity <MetadataObject> -Path <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-LocalizedNamesIncluded <SwitchParameter>] [-ModelsIncluded <SwitchParameter>] [-PermissionsIncluded <SwitchParameter>] [-PropertiesIncluded <SwitchParameter>] [-SettingId <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Import-SPBusinessDataCatalogModel** cmdlet imports a Business Data Connectivity Model. There are two types of Business Data Connectivity models: **Model** type (.bdcm) and **Resource** type (.bdcr). The **Model** type contains the base XML metadata, and can also include resource properties. The **Resource** type includes only resource properties. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.Administration.MetadataObject  <br/> |Specifies the Business Data Connectivity Metadata Store metadata object to import to.  <br/> |
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies the path and name to use.  <br/> The type must be a valid path in either of the following forms:  <br/> - C:\folder_name\file.bdcm  <br/> - \\server_name\folder_name\file.bdcm  <br/> - …\folder_name\file.bdcm  <br/> |
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context to set.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Overwrites the Business Data Connectivity Model if the file exists.  <br/> |
|**LocalizedNamesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that names for business data fields in multiple languages are imported.  <br/> |
|**ModelsIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that models are included in the imported Business Data Connectivity Model file. A model contains the base XML metadata for a system.  <br/> |
|**PermissionsIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that permissions from the Business Data Connectivity Model are imported.  <br/> |
|**PropertiesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that properties from the Business Data Connectivity Model are imported.  <br/> |
|**SettingId** <br/> |Optional  <br/> |System.String  <br/> |Specifies the custom environment settings model slice to import.  <br/> The type must be a valid string that identifies a model slice; for example, ModelSlice1.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.Administration.MetadataObject  <br/> ||
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**LocalizedNamesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ModelsIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**PermissionsIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**PropertiesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SettingId** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1------------------
  
```
$MetadataStore = Get-SPBusinessDataCatalogMetadataObject -BdcObjectType "Catalog" -ServiceContext http://contoso
```

```
Import-SPBusinessDataCatalogModel -Path "C:\folder\model.bdcm" -Identity $MetadataStore
```

This example gets the Business Data Connectivity Metadata Store and then imports a Business Data Connectivity Model of **Model** type to it from the path specified with the name  `model`.
  
------------------EXAMPLE 2------------------
  
```
Import-SPBusinessDataCatalogModel -Path "C:\Program Files\Duet Enterprise\2.0\BDC Models\Reporting.en-us.bdcr -Identity $bdcCatalog -ModelsIncluded:$false 
```

This example imports a resource only file by using the **ModelsIncluded** parameter. 
  
## See also

#### 

[Export-SPBusinessDataCatalogModel](export-spbusinessdatacatalogmodel.md)
  
[Remove-SPBusinessDataCatalogModel](remove-spbusinessdatacatalogmodel.md)

