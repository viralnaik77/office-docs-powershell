---
title: "Remove-SPClaimTypeMapping"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3c90d1a-de69-4387-860f-be756efbbcfb

description: "Deletes a claim type mapping rule for a security token service (STS) identity provider."
---

# Remove-SPClaimTypeMapping

Deletes a claim type mapping rule for a security token service (STS) identity provider.
  
```
Remove-SPClaimTypeMapping [-Identity] <SPClaimMappingPipeBind> [-TrustedIdentityTokenIssuer] <SPTrustedIdentityTokenIssuerPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPClaimMapping** cmdlet deletes a claim type mapping rule from a farm trust STS identity provider. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPClaimMappingPipeBind  <br/> |Specifies the claim mapping to delete.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of a claim mapping rule (for example, Email); or an instance of a valid **SPClaimMapping** object.  <br/> |
|**TrustedIdentityTokenIssuer** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> |Specifies the token issuer or a valid **SPTrustedIdentityTokenIssuerPipeBind** object.  <br/> |
|**IdentityProvider** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> |Specifies the farm trust identity provider STS that contains the claim mapping rule.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of identity provider (for example, LiveIDSTS); or an instance of a valid **SPTrustedIdentityTokenIssuerPipeBind** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPClaimMappingPipeBind  <br/> ||
|**TrustedIdentityTokenIssuer** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------------EXAMPLE-------------------------
  
```
Remove-SPClaimMapping -Identity "Email" - TrustedIdentityTokenIssuer "LiveIDSTS"
```

This example removes the claim mapping  `EMAIL` from an identity provider named  `LiveIDSTS`.
  
## See also

#### 

[Add-SPClaimTypeMapping](add-spclaimtypemapping.md)
  
[New-SPClaimTypeMapping](new-spclaimtypemapping.md)

