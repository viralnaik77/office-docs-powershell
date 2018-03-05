---
title: "Export-SPBusinessDataCatalogModel"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6008afe4-89f9-4b50-908d-aa47c6368374

description: "Exports a Business Data Connectivity Model."
---

# Export-SPBusinessDataCatalogModel

Exports a Business Data Connectivity Model.
  
```
Export-SPBusinessDataCatalogModel -Identity <MetadataObject> -Path <String> [-AssignmentCollection <SPAssignmentCollection>] [-Force <SwitchParameter>] [-LocalizedNamesIncluded <SwitchParameter>] [-ModelsIncluded <SwitchParameter>] [-PermissionsIncluded <SwitchParameter>] [-PropertiesIncluded <SwitchParameter>] [-ProxiesIncluded <SwitchParameter>] [-SettingId <String>]
```

## Detailed Description

The **Export-SPBusinessDataCatalogModel** cmdlet exports a Business Data Connectivity Model. There are two types of Business Data Connectivity models: **Model** type (.bdcm) and **Resource** type (.bdcr). The **Model** type contains the base XML metadata, and can also include resource properties. The **Resource** type includes only resource properties. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.Administration.MetadataObject  <br/> |Specifies the Business Data Connectivity Metadata Store metadata object from which to export the Business Data Connectivity Model.  <br/> |
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies the path and name to use to create the export file.  <br/> The type must be a valid path in either of the following forms:  <br/> - C:\folder_name \file.bdcm  <br/> - \\server_name\folder_name \file.bdcm  <br/> - …\folder_name\file.bdcm  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Overwrites the output file if the file exists.  <br/> |
|**LocalizedNamesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that names for business data fields in multiple languages are exported.  <br/> |
|**ModelsIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that models are included in the exported Business Data Connectivity Model file. A model contains the base XML metadata for a system.  <br/> |
|**PermissionsIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that permissions from the Business Data Connectivity Model are exported.  <br/> |
|**PropertiesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that properties from the application definition are exported.  <br/> |
|**ProxiesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that proxies for Business Data Connectivity Service applications are exported.  <br/> |
|**SettingId** <br/> |Optional  <br/> |System.String  <br/> |Specifies the custom environment settings model slice to export.  <br/> The type must be a valid string that identifies a model slice; for example, ModelSlice1.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.Administration.MetadataObject  <br/> ||
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**LocalizedNamesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ModelsIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**PermissionsIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**PropertiesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ProxiesIncluded** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SettingId** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$Model = Get-SPBusinessDataCatalogMetadataObject -BdcObjectType "Model" -Name "ContosoModel" -ServiceContext http://contoso
```

```
Export-SPBusinessDataCatalogModel -Identity $Model -Path "C:\folder\model.bdcm"
```

This example gets a Business Data Connectivity Model from the Business Data Connectivity Metadata Store and exports it to the location specified with the name  `model` and using the  `bdcm` file extension. 
  
## See also

#### 

[Import-SPBusinessDataCatalogModel](import-spbusinessdatacatalogmodel.md)
  
[Remove-SPBusinessDataCatalogModel](remove-spbusinessdatacatalogmodel.md)

