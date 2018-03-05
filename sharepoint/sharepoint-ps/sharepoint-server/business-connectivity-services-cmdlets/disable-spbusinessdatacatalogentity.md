---
title: "Disable-SPBusinessDataCatalogEntity"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f552241-a609-47e3-b07f-8e51b7fd585c

description: "Deactivates an External Content type in the Business Data Connectivity Metadata Store."
---

# Disable-SPBusinessDataCatalogEntity

Deactivates an External Content type in the Business Data Connectivity Metadata Store.
  
```
Disable-SPBusinessDataCatalogEntity -Identity <Entity> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Disable-SPBusinessDataCatalogEntity** cmdlet deactivates an External Content type in the Business Data Connectivity Metadata Store. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.Administration.Entity  <br/> |Specifies the External Content type in the Business Data Connectivity Metadata Store to deactivate.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|||||
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.Administration.Entity  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$entityToDisable = Get-SPBusinessDataCatalogMetadataObject -Namespace "Contoso" -Name "Customer" -BdcObjectType "Entity" -ServiceContext http://contoso
```

```
Disable-SPBusinessDataCatalogEntity -Identity $entityToDisable
```

This example deactivates the External Content type of the name  `Customer` in the  `Contoso`. Note that the terms External Content type and **Entity** refer to the same object type, and the term **Disable** refers to the same action as the Business Data Connectivity term **Deactivate**.
  
## See also

#### 

[Enable-SPBusinessDataCatalogEntity](enable-spbusinessdatacatalogentity.md)

