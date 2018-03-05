---
title: "Add-SPClaimTypeMapping"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/20/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9d2de49a-bc77-495b-9698-6dc9b7058867

description: "Adds a claim mapping to a trusted security token service (STS) identity provider."
---

# Add-SPClaimTypeMapping

Adds a claim mapping to a trusted security token service (STS) identity provider.
  
```
Add-SPClaimTypeMapping [-Identity] <SPClaimMappingPipeBind> [-TrustedIdentityTokenIssuer] <SPTrustedIdentityTokenIssuerPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Force <SwitchParameter>]
```

## Detailed Description

The **Add-SPClaimTypeMapping** cmdlet adds a claim type mapping rule to a security token service (STS) identity provider from a farm trust STS authentication provider. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPClaimMappingPipeBind  <br/> |Specifies the STS for the farm that will issue the security token for the identity provider.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of a claim mapping rule (for example, ClaimMap1); or an instance of a valid **SPClaimMapping** object.  <br/> |
|**TrustedIdentityTokenIssuer** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> |Specifies the farm trust Token Issuer (STS authentication provider).  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of an authentication provider (for example, MyIDprovider1); or an instance of a valid **SPTrustedIdentityTokenIssuer** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Overwrites the claim mapping rule if it exists.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPClaimMappingPipeBind  <br/> ||
|**TrustedIdentityTokenIssuer** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Get-TrustedIdentityTokenIssuer -Identity "LiveIDSTS" | Add-SPClaimTypeMapping -IncomingClaimType "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier" -IncomingClaimTypeDisplayName "PUID" -LocalClaimType "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/thumbprint"
```

This example adds a claim mapping to a trusted identity token issuer.
  
## See also

#### 

[New-SPClaimTypeMapping](new-spclaimtypemapping.md)
  
[Remove-SPClaimTypeMapping](remove-spclaimtypemapping.md)

