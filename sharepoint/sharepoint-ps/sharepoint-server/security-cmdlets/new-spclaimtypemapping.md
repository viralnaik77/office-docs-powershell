---
title: "New-SPClaimTypeMapping"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 57549b89-8335-4224-b075-cacd80e26862

description: "Creates a claim mapping rule for a security token service (STS) identity provider."
---

# New-SPClaimTypeMapping

Creates a claim mapping rule for a security token service (STS) identity provider.
  
```
New-SPClaimTypeMapping [-IncomingClaimType] <String> [-IncomingClaimTypeDisplayName] <String> [[-LocalClaimType] <String>] [-AssignmentCollection <SPAssignmentCollection>] [-SameAsIncoming <SwitchParameter>]
```

## Detailed Description

The **New-SPClaimTypeMapping** cmdlet creates a claim mapping rule for a security token service (STS) identity provider. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**IncomingClaimType** <br/> |Required  <br/> |System.String  <br/> |Specifies the URI of the incoming claim type.  <br/> The type must be a valid URI, in the form http://schemas.microsoft.com/email.  <br/> |
|**IncomingClaimTypeDisplayName** <br/> |Required  <br/> |System.String  <br/> |Specifies the display name of the incoming claim type.  <br/> The type must be a valid name of an incoming claim type; for example, Email.  <br/> |
|**LocalClaimType** <br/> |Optional  <br/> |System.String  <br/> |Specifies the URI of the local claim type. If the **SameAsIncoming** parameter is False, this is a required parameter.  <br/> The type must be a valid URI, in the form http://schemas.microsoft.com/email.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**SameAsIncoming** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the claim type specified in the **IncomingClaimType** parameter is used for the **LocalClaimType** parameter.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**IncomingClaimType** <br/> |Required  <br/> |System.String  <br/> ||
|**IncomingClaimTypeDisplayName** <br/> |Required  <br/> |System.String  <br/> ||
|**LocalClaimType** <br/> |Optional  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**SameAsIncoming** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------------EXAMPLE 1---------------------------- 
  
```
$map1 = New-SPClaimTypeMapping -IncomingClaimType "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress" -IncomingClaimTypeDisplayName "EmailAddress" -SameAsIncoming
```

```
$map2 = New-SPClaimTypeMapping -IncomingClaimType "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier" -IncomingClaimTypeDisplayName "PUID" -LocalClaimType "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/thumbprint"
```

```
New-SPTrustedIdentityTokenIssuer -Name "LiveIDSTS" -Description "LiveID Provider" -Realm "urn:domain.company.com" -ImportTrustCertificate $cert -ClaimsMappings $map1[,$map2..] -SignInUrl "https://login.live.com/login.srf" -IdentifierClaim $map2.InputClaimType
```

This example creates a claim map from an incoming token to a SharePoint token.
  
## See also

#### 

[Add-SPClaimTypeMapping](add-spclaimtypemapping.md)
  
[Remove-SPClaimTypeMapping](remove-spclaimtypemapping.md)

