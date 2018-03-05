---
title: "New-SPClaimsPrincipal"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0831e64b-3ec0-4016-8128-639991530172

description: "Creates a claims principal."
---

# New-SPClaimsPrincipal

Creates a claims principal.
  
```
New-SPClaimsPrincipal [-Identity] <String> [-IdentityType] <WindowsSamAccountName | WindowsSecurityGroupName | WindowsSecurityGroupSid | FormsUser | FormsRole | EncodedClaim> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **New-SPClaimsPrincipal** cmdlet creates a claims principal. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ClaimValue** <br/> |Required  <br/> |System.String  <br/> |Specifies the claim value of the claims object. The claims value specifies the user, group, or computer that the claim is authenticating.  <br/> The type must be a valid claim value; for example, john@contoso.com.  <br/> |
|**EncodedClaim** <br/> |Required  <br/> |System.String  <br/> |Converts a simple claim to a full encoded claim.  <br/> The type must be a valid claim value; for example, i:001w|redmond\user.  <br/> |
|**Identity** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the new claims principal.  <br/> The type must be a valid name of a claims principal.  <br/> |
|**ClaimType** <br/> |Required  <br/> |System.String  <br/> |Specifies the type of claim to create. The value I indicates a unique user identity claim, and the value C indicates all other claims.  <br/> The type must be either of the following values: I or C.  <br/> |
|**TrustedIdentityTokenIssuer** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> |Specifies the ID of the authentication provider.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of an Authentication provider (for example, MyAuthprovider1); or an instance of a valid **SPTrustedIdentityTokenIssuer** object.  <br/> |
|**IdentityType** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.Claims.SPIdentifierTypes  <br/> |Specifies the type of the new claims principal.  <br/> The type must be one of the following: **WindowsSamAccountName**, **WindowsSecurityGroupSid**, **FormsUser**, **FormsRole**, or **EncodedClaim**.  <br/> |
|**ClaimProvider** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaimProvider  <br/> |Specifies the security token service identity provider that will contain the claims principal.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of identity provider (for example, MyIDprovider1); or an instance of a valid **SPIdentityProvider** object.  <br/> |
|**IdentifierClaim** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies if the new claim is an identity claim.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ClaimValue** <br/> |Required  <br/> |System.String  <br/> ||
|**EncodedClaim** <br/> |Required  <br/> |System.String  <br/> ||
|**Identity** <br/> |Required  <br/> |System.String  <br/> ||
|**ClaimType** <br/> |Required  <br/> |System.String  <br/> ||
|**IdentityType** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.Claims.SPIdentifierTypes  <br/> ||
|**TrustedIdentityTokenIssuer** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> ||
|**ClaimProvider** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaimProvider  <br/> ||
|**IdentifierClaim** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-------------------------EXAMPLE 1-----------------------------
  
```
New-SPSite http://sitename/sites/newsite -owner (New-SPClaimsPrincipal contoso\johndoe -TrustedIdentityTokenIssuer "NTLM")
```

This example creates a claim principal for a Windows user.
  
-------------------------EXAMPLE 2-----------------------------
  
```
New-SPSite http://localhost/sites/newsite -owner (New-SPClaimsPrincipal contoso\allusers -TrustedIdentityTokenIssuer "NTLM")
```

This example creates a claim principal for a Windows group.
  
-------------------------EXAMPLE 3-----------------------------
  
```
New-SPSite http://sitename/sites/newsite -owner (New-SPClaimsPrincipal -ClaimValue "john@contoso.com" -ClaimType Email -TrustedIdentityTokenIssuer "LiveID STS" -IdentifierClaim Yes)
```

This example creates a claim principal for a trusted identity token issuer claim.
  
-------------------------EXAMPLE 4-----------------------------
  
```
$ip = New-SPIdentityProvider -ASPNetMembershipProvider "myMembershipProvider" -ASPNetRoleProvider "myRoleProvider"
```

```
New-SPSite http://sitename/sites/newsite -owner (New-SPClaimsPrincipal "john@contoso.com" -TrustedIdentityTokenIssuer $ip)
```

This example creates a claim principal for a ASPNet Membership User.
  
-------------------------EXAMPLE 5-----------------------------
  
```
New-SPSite http://sitename/sites/newsite -owner (New-SPClaimsPrincipal "Sales Manager Role" -IdentityProvider "myRoleProvider")
```

This example creates a claim principal for a ASPNet Role.
  
-------------------------EXAMPLE 6-----------------------------
  
```
 $cp = New-SPClaimsPrincipal -Identity "redmond\SiteOwner" -IdentityType 1
```

```
New-SPSite http://servername:port -OwnerAlias $cp.ToEncodedString() -Template "STS#0"
```

This example creates a claim principal for a Basic Claim Role, which is also called an encoded claim).
  

