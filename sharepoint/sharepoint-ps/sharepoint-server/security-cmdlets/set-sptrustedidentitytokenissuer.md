---
title: "Set-SPTrustedIdentityTokenIssuer"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/7/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9259e179-50fd-4da1-ad48-33d241b5f44a

description: "Sets the identity providers of a Web application."
---

# Set-SPTrustedIdentityTokenIssuer

Sets the identity providers of a Web application.
  
```
Set-SPTrustedIdentityTokenIssuer -Identity <SPTrustedIdentityTokenIssuerPipeBind> -MetadataEndPoint <Uri> [-ClaimProvider <SPClaimProviderPipeBind>] [-ClaimsMappings <SPClaimMappingPipeBind[]>] [-Description <String>] [-Realm <String>] [-RegisteredIssuerName <String>] [-SignInUrl <String>] [-UseWReply <SwitchParameter>] <COMMON PARAMETERS>

```

## Example

-------------------------EXAMPLE 1---------------------- 
  
```
Set-SPTrustedIdentityTokenIssuer "LiveIDSTS" -ImportTrustCertificate (Get-ChildItem"cert:Certificates (LocalComputer)\Personal\Certificates -Name "LiveID Cert")
```

This example sets the identity provider to  `LiveIDSTS`.
  
-------------------------EXAMPLE 2---------------------- 
  
```
$ip = @( (Get-SPTrustedIdentityTokenIssuer "LiveID STS"), (New-SPTrustedIdentityTokenIssuer -ASPNetMembershipProvider "myMembershipProvider" -ASPNetRoleProvider "myRoleProvider"), (Get-SPTrustedIdentityTokenIssuer "NTLM")) )New-SPWebApplication http://contoso.com -IdentityProvider $ip
```

This example sets the identity provider using the **.ASPNetMembership** and **Role** parameters. When these parameters are used, a variable must be set; otherwise, the values do not take effect. 
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Set-SPTrustedIdentityTokenIssuer** cmdlet sets the identity providers of a Web application or extended Web application. For the ASP.NET Membership provider and Role provider, this cmdlet changes the identity provider only if the result is piped to a variable and passed to a Web application. For security token service (STS) identity providers, this cmdlet changes the persisted identity provider object in the **SPFarm** object. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> |Specifies the identity provider to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of identity provider (for example, LiveID STS); or an instance of a valid **SPIdentityProvider** object.  <br/> |
| _ImportTrustCertificate_ <br/> |Required  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> |Specifies the X.509 certificate object from trusted authentication provider farm.  <br/> The type must be a name of a valid X.509 certificate; for example, Certificate1.  <br/> |
| _MetadataEndPoint_ <br/> |Required  <br/> |System.Uri  <br/> |Specifies the URI for the metadata endpoint of the trusted provider.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _ClaimProvider_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPClaimProviderPipeBind  <br/> |Specifies the IP STS that can resolve and search claims for claims people picker.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of a claim provider (for example, MyIDprovider1); or an instance of a valid **SPClaimProvider** object.  <br/> |
| _ClaimsMappings_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPClaimMappingPipeBind[]  <br/> |Specifies the mapping of the claims from the original token to the SharePoint token.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of a claim mapping rule (for example, Email); or an instance of a valid **SPClaimMapping** object.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Description_ <br/> |Optional  <br/> |System.String  <br/> |Specifies a description for the new identity provider.  <br/> The type must be a valid string; for example, LiveID STS.  <br/> |
| _Realm_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the realm, or resource partition, associated with this trust.  <br/> The type must be a name of a valid realm; for example, MD_REALM.  <br/> |
| _RegisteredIssuerName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the Registered Issuer Name instead of not using the metadata endpoint.  <br/> |
| _SignInUrl_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the sign-in URLs for this trusted identity provider STS.  <br/> The type must be a valid URL, in the form http://int.live.com/.  <br/> |
| _UseWReply_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Includes a WReply with the token request. Wreply is a URL at the relying party to which the requestor is redirected once sign-out processing is complete.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**ClaimProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPClaimProviderPipeBind  <br/> ||
|**ClaimsMappings** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPClaimMappingPipeBind[]  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Description** <br/> |Optional  <br/> |System.String  <br/> ||
|**ImportTrustCertificate** <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> ||
|**MetadataEndPoint** <br/> |Optional  <br/> |System.Uri  <br/> ||
|**Realm** <br/> |Optional  <br/> |System.String  <br/> ||
|**SignInUrl** <br/> |Optional  <br/> |System.String  <br/> ||
|**UseWReply** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPTrustedIdentityTokenIssuer](get-sptrustedidentitytokenissuer.md)
  
[New-SPTrustedIdentityTokenIssuer](new-sptrustedidentitytokenissuer.md)
  
[Remove-SPTrustedIdentityTokenIssuer](remove-sptrustedidentitytokenissuer.md)

