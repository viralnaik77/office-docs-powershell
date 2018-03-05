---
title: "Set-SPBusinessDataCatalogMetadataObject"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e7a2a1a9-b2c3-4303-bf82-11d90f1eedf5

description: "Sets the value of a property or attribute of a Business Data Connectivity Metadata Store metadata object."
---

# Set-SPBusinessDataCatalogMetadataObject

Sets the value of a property or attribute of a Business Data Connectivity Metadata Store metadata object.
  
```
Set-SPBusinessDataCatalogMetadataObject -Identity <MetadataObject> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-PropertyName <String>] [-PropertyValue <PSObject>] [-Remove <SwitchParameter>] [-SettingId <String>] [-WhatIf [<SwitchParameter>]]

```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Set-SPBusinessDataCatalogMetadataObject** cmdlet sets the value of a property or attribute of a Business Data Connectivity Metadata Store metadata object. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.Administration.MetadataObject  <br/> |Specifies the Business Data Connectivity Metadata Store metadata object to update.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DisplayName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the display name of the Business Data Connectivity Metadata Store metadata object.  <br/> |
|**PropertyName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the property to update.  <br/> |
|**PropertyValue** <br/> |Optional  <br/> |System.Management.Automation.PSObject  <br/> |Sets the new value of the property specified in the **PropertyName** parameter.  <br/> |
|**Remove** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Removes the property specified in the **PropertyName** parameter.  <br/> |
|**SettingId** <br/> |Optional  <br/> |System.String  <br/> |Specifies the custom environment settings model slice for which the property applies.  <br/> The type must be a valid string that identifies a model slice; for example, ModelSlice1.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.Administration.MetadataObject  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DisplayName** <br/> |Optional  <br/> |System.String  <br/> ||
|**PropertyName** <br/> |Optional  <br/> |System.String  <br/> ||
|**PropertyValue** <br/> |Optional  <br/> |System.Management.Automation.PSObject  <br/> ||
|**Remove** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SettingId** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1------------------
  
```
$objectToSetOn = Get-SPBusinessDataCatalogMetadataObject -Namespace "ContosoDatabase" -Name "ContosoDatabase" -BdcObjectType "LobSystemInstance" -ServiceContext http://contoso
```

```
Set-SPBusinessDataCatalogMetadataObject -Identity $objectToSetOn -PropertyName "ShowInSearchUI" -PropertyValue "True"
```

This example creates a property on the  `LobSystemInstance` (External System Instance) of name  `ContosoDatabase`. The property has the name  `ShowInSearchUI` and a value of  `True`.
  
## See also

#### 

[Get-SPBusinessDataCatalogMetadataObject](get-spbusinessdatacatalogmetadataobject.md)
  
[Revoke-SPBusinessDataCatalogMetadataObject](revoke-spbusinessdatacatalogmetadataobject.md)
  
[Grant-SPBusinessDataCatalogMetadataObject](grant-spbusinessdatacatalogmetadataobject.md)

