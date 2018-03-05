---
title: "Copy-SPBusinessDataCatalogAclToChildren"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1d2d579a-5998-473f-83b8-25f030de3da5

description: "Copies a set of permissions of a Business Data Connectivity Metadata Store metadata object to its child objects."
---

# Copy-SPBusinessDataCatalogAclToChildren

Copies a set of permissions of a Business Data Connectivity Metadata Store metadata object to its child objects.
  
```
Copy-SPBusinessDataCatalogAclToChildren -MetadataObject <MetadataObject> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Copy-SPBusinessDataCatalogAclToChildren** cmdlet copies a set of rights of a Business Data Connectivity metadata object to its child objects. 
  
Any principals and their rights will be lost from the child metadata objects. Make sure that the parent metadata object has the final permissions you want, or make sure to append them to the child object again after you run this cmdlet.
  
Running this cmdlet on a **BdcObjectType BdcCatalog** (Business Data Connectivity Metadata Store) will propagate to: 
  
- BDC Models
  
- External Systems
  
- External Content Types
  
- Methods
  
- Method Instances
  
Running this cmdlet on a **BdcObjectType** Model (Business Data Connectivity Model) will propagate to: 
  
- Nothing; this type has no child metadata objects
  
Running this cmdlet on a **BdcObjectType LobSystem** (External System) will propagate to: 
  
- External Content Types
  
- Methods
  
- Method Instances
  
Running this cmdlet on a **BdcObjectType Entity** (External Content Type) will propagate to: 
  
- Methods
  
- Method Instances
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**MetadataObject** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.Administration.MetadataObject  <br/> |Specifies the Business Data Connectivity metadata object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**MetadataObject** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.Administration.MetadataObject  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$ExternalSystem = Get-SPBusinessDataCatalogMetadataObject -BdcObjectType "LobSystem" -ServiceContext http://contoso -Name "ContosoDatabase"
```

This example looks at the principals (users) and their corresponding rights given for the **External System** metadata object, and overwrites the permissions of its child metadata objects with these same principals and rights. 
  
Any principals and their rights will be lost from the child metadata objects. Make sure that the parent metadata object has the final permissions you want, or make sure to append them to the child object again after you run this cmdlet.
  
## See also

#### 

[Get-SPBusinessDataCatalogMetadataObject](get-spbusinessdatacatalogmetadataobject.md)
  
[Grant-SPBusinessDataCatalogMetadataObject](grant-spbusinessdatacatalogmetadataobject.md)

