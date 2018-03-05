---
title: "New-SPTrustedIdentityTokenIssuer"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/7/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 436b2743-c358-46c3-9d9e-9eb37daee85d

description: "Creates an identity provider in the farm."
---

# New-SPTrustedIdentityTokenIssuer

Creates an identity provider in the farm.
  
```
New-SPTrustedIdentityTokenIssuer -ClaimsMappings <SPClaimMappingPipeBind[]> -Description <String> -IdentifierClaim <String> -Name <String> -Realm <String> -SignInUrl <String> [-ClaimProvider <SPClaimProviderPipeBind>] [-ImportTrustCertificate <X509Certificate2>] [-RegisteredIssuerName <String>] [-SignOutUrl <String>] [-UseWReply <SwitchParameter>] <COMMON PARAMETERS>

```

## Example

----------------------- EXAMPLE---------------------------
  
```
New-SPTrustedIdentityTokenIssuer -Name "LiveIDSTS" - Description "LiveID STS" - ImportTrustCertificate (Get-ChildItem"cert:Certificates (LocalComputer)\Personal\Certificates -Name "LiveID Cert") -SignInUrl http://int.contoso.com/ -IdentifierClaim "http://schemas.contoso.com/2007/05/Claims/Puid"
```

```
Set -SPWebApplication http://contoso.com -IdentityProvider (Get-SPTrustedIdentityTokenIssuer "LiveIDSTS")
```

This example creates a new identity provider in the farm named  `LiveIDSTS`.
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **New-SPTrustedIdentityTokenIssuer** cmdlet creates an identity provider in the farm. This object is created and used only for setting this type of identity provider in a Web application. The specified claim type cannot be **NTLM**, **Classic NTLM**, **Negotiate**, or **Classic Negotiate**. For ASP.NET Membership provider or Role providers, no objects are persisted. For security token service (STS) identity providers, this cmdlet creates and persists the identity provider object in the **SPFarm** object. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ClaimsMappings_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPClaimMappingPipeBind[]  <br/> |Specifies the mapping of the claims from the original token to the SharePoint token.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of a claim mapping rule (for example, Email); or an instance of a valid **SPClaimMapping** object.  <br/> |
| _Description_ <br/> |Required  <br/> |System.String  <br/> |Specifies a description for the new identity provider.  <br/> The type must be a valid string; for example, LiveID STS.  <br/> |
| _IdentifierClaim_ <br/> |Required  <br/> |System.String  <br/> |Specifies which claim type from the trusted STS will be used for the new identity provider.  <br/> The type must be a valid claim type from the trusted STS; for example, http://schemas.microsoft.com/2007/05/Claims/Puid.  <br/> |
| _MetadataEndPoint_ <br/> |Required  <br/> |System.Uri  <br/> |Specifies the URI for the metadata endpoint of the trusted provider.  <br/> |
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the new identity provider.  <br/> The type must be a valid name of an identity provider; for example, LiveIDSTS.  <br/> |
| _Realm_ <br/> |Required  <br/> |System.String  <br/> |Specifies the realm, or resource partition, associated with this trust.  <br/> The type must be a name of a valid realm; for example, MD_REALM.  <br/> |
| _SignInUrl_ <br/> |Required  <br/> |System.String  <br/> |Specifies the sign-in URLs for this trusted STS identity provider.  <br/> The type must be a valid URL, in the form http://int.live.com/.  <br/> |
| _UseDefaultConfiguration_ <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies if the default set of claim mappings should be used.  <br/> If **UseDefaultConfiguration** parameter is used, then the **IdentifierClaimIs** parameter must be used.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _ClaimProvider_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPClaimProviderPipeBind  <br/> |Specifies the IP STS that can resolve and search claims for claims people picker.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of identity provider (for example, MyIDprovider1); or an instance of a valid **SPIdentityProvider** object.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _IdentifierClaimIs_ <br/> |Optional  <br/> |System.String  <br/> |Specifies which of the default mapped claims should be used as the identifier claim.  <br/> Only used if the **UseDefaultConfiguration** parameter is set to true, otherwise use the **IdentifierClaim** parameter.  <br/> |
| _ImportTrustCertificate_ <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> |Specifies the X.509 certificate object from trusted authentication provider farm.  <br/> The type must be a name of a valid X.509 certificate; for example, Certificate1.  <br/> |
| _RegisteredIssuerName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the Registered Issuer Name instead of not using the metadata endpoint.  <br/> |
| _SignOutUrl_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the sign out URI for the trusted provider. This lets SharePoint to sign the user out from the trusted provider when they sign out from SharePoint.  <br/> |
| _UseWReply_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Includes a **WReply** with the token request. **WReply** is a URL at the relying party to which the requestor is redirected once sign-out processing is complete.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ClaimsMappings** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPClaimMappingPipeBind[]  <br/> ||
|**Description** <br/> |Required  <br/> |System.String  <br/> ||
|**IdentifierClaim** <br/> |Required  <br/> |System.String  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**Realm** <br/> |Required  <br/> |System.String  <br/> ||
|**SignInUrl** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**ClaimProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPClaimProviderPipeBind  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ImportTrustCertificate** <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> ||
|**MetadataEndPoint** <br/> |Optional  <br/> |System.Uri  <br/> ||
|**UseWReply** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPTrustedIdentityTokenIssuer](get-sptrustedidentitytokenissuer.md)
  
[Set-SPTrustedIdentityTokenIssuer](set-sptrustedidentitytokenissuer.md)
  
[Remove-SPTrustedIdentityTokenIssuer](remove-sptrustedidentitytokenissuer.md)

