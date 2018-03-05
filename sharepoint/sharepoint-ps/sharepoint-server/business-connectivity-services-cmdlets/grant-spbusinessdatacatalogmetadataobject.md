---
title: "Grant-SPBusinessDataCatalogMetadataObject"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 99b2fdb9-8a20-430f-b6a4-f56c9f2a67b7

description: "Grants a right to a principal for the specified Business Data Connectivity Metadata Store metadata object."
---

# Grant-SPBusinessDataCatalogMetadataObject

Grants a right to a principal for the specified Business Data Connectivity Metadata Store metadata object.
  
```
Grant-SPBusinessDataCatalogMetadataObject -Identity <MetadataObject> -Principal <SPClaim> -Right <Execute | Edit | SetPermissions | SelectableInClients> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-SettingId <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Grant-SPBusinessDataCatalogMetadataObject** cmdlet grants the right to a specified principal (user) for a Business Data Connectivity Metadata Store metadata object. This cmdlet checks to verify that the **Identity** parameter is a valid **IndividuallySecurableMetadata** object. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.Administration.MetadataObject  <br/> |Specifies the Business Data Connectivity Metadata Store metadata object that contains the principal.  <br/> |
|**Principal** <br/> |Required  <br/> |System.String  <br/> |Specifies the principal to whom the rights apply.  <br/> The type must be a claim.  <br/> |
|**Right** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.SharedService.SPGrantSPBusinessDataCatalogMetadataObjectCmdlet+PSBdcRight  <br/> |Specifies the right to grant the principal.  <br/> The type must be one of the following valid **PSBdcRight** object types: **All**, **Execute**, **Edit**, **SetPermissions**, or **SelectableInClients**.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**SettingId** <br/> |Optional  <br/> |System.String  <br/> |Specifies the model slice for which to grant the right.  <br/> The type must be a valid string that identifies a model slice; for example, ModelSlice1.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.Administration.MetadataObject  <br/> ||
|**Principal** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim  <br/> ||
|**Right** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.SharedService.SPGrantSPBusinessDataCatalogMetadataObjectCmdlet+PSBdcRight  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SettingId** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$claimJohn = New-SPClaimsPrincipal -Identity "CONTOSO\johndoe" -IdentityType WindowsSamAccountName
```

```
$Model = Get-SPBusinessDataCatalogMetadataObject -BdcObjectType "Model" -ServiceContext http://contoso -Name "ContosoModel"
```

```
Grant-SPBusinessDataCatalogMetadataObject -Identity $Model -Principal $claimJohn -Right Edit
```

This example gives  `Edit` permissions to the user with the identity  `johndoe` on domain  `CONTOSO`, for the model metadata object with the name  `ContosoModel`.
  
## See also

#### 

[Set-SPBusinessDataCatalogMetadataObject](set-spbusinessdatacatalogmetadataobject.md)
  
[Get-SPBusinessDataCatalogMetadataObject](get-spbusinessdatacatalogmetadataobject.md)
  
[Revoke-SPBusinessDataCatalogMetadataObject](revoke-spbusinessdatacatalogmetadataobject.md)

