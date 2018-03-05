---
title: "Use Windows PowerShell cmdlets to administer security in SharePoint Server 2016"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 2/29/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: 30199c87-cd44-43ef-af68-7cfd9d2b4101
description: "Summary: Learn about the Windows PowerShell cmdlets that you can use to administer security for SharePoint Server 2016 Release Candidate."
---

# Use Windows PowerShell cmdlets to administer security in SharePoint Server 2016

 **Summary:** Learn about the Windows PowerShell cmdlets that you can use to administer security for SharePoint Server 2016 Release Candidate. 
  
The following table shows the Microsoft PowerShell cmdlets that you can use to administer security for SharePoint Server 2016.
  
|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Add-SPShellAdmin](add-spshelladmin.md)** <br/> |Adds a user to the **SharePoint_Shell_Access** role for the specified database.  <br/> |
|**[Get-SPShellAdmin](get-spshelladmin.md)** <br/> |Returns the names of all users who have the **SharePoint_Shell_Access** role.  <br/> |
|**[Remove-SPShellAdmin](remove-spshelladmin.md)** <br/> |Removes a user from the **SharePoint_Shell_Access** role.  <br/> |
|**[Add-SPClaimTypeMapping](add-spclaimtypemapping.md)** <br/> |Adds a claim mapping to a trusted security token service (STS) identity provider.  <br/> |
|**[Get-SPAuthenticationProvider](get-spauthenticationprovider.md)** <br/> |Returns an authentication provider.  <br/> |
|**[Get-SPCertificateAuthority](get-spcertificateauthority.md)** <br/> |Returns the SharePoint certificate authority (CA).  <br/> |
|**[Get-SPClaimProvider](get-spclaimprovider.md)** <br/> |Returns a claim provider.  <br/> |
|**[Get-SPClaimProviderManager](get-spclaimprovidermanager.md)** <br/> |Returns a claim provider manager.  <br/> |
|**[Get-SPClaimTypeEncoding](get-spclaimtypeencoding.md)** <br/> |Returns a list of all the types of claims.  <br/> |
|**[Get-SPManagedAccount](get-spmanagedaccount.md)** <br/> |Retrieves accounts registered in the configuration database.  <br/> |
|**[Get-SPManagedPath](get-spmanagedpath.md)** <br/> |Returns all managed paths that match the given criteria.  <br/> |
|**[Get-SPSecurityTokenServiceConfig](get-spsecuritytokenserviceconfig.md)** <br/> |Returns the security token service (STS) for the farm.  <br/> |
|**[Get-SPServiceApplicationSecurity](get-spserviceapplicationsecurity.md)** <br/> |Returns the **SPObjectSecurity** object for a service application.  <br/> |
|**[Get-SPTrustedIdentityTokenIssuer](get-sptrustedidentitytokenissuer.md)** <br/> |Returns an identity provider.  <br/> |
|**[Get-SPTrustedRootAuthority](get-sptrustedrootauthority.md)** <br/> |Returns a trusted root authority.  <br/> |
|**[Get-SPTrustedServiceTokenIssuer](get-sptrustedservicetokenissuer.md)** <br/> |Returns the object that represents the farm trust.  <br/> |
|**[Grant-SPObjectSecurity](grant-spobjectsecurity.md)** <br/> |Adds a new security principal to an **SPObjectSecurity** object.  <br/> |
|**[Initialize-SPResourceSecurity](initialize-spresourcesecurity.md)** <br/> |Enforces resource security on the local server.  <br/> |
|**[New-SPAuthenticationProvider](new-spauthenticationprovider.md)** <br/> |Creates a new authentication provider in the farm.  <br/> |
|**[New-SPClaimProvider](new-spclaimprovider.md)** <br/> |Registers a new claim provider in the farm.  <br/> |
|**[New-SPClaimsPrincipal](new-spclaimsprincipal.md)** <br/> |Creates a new claims principal.  <br/> |
|**[New-SPClaimTypeEncoding](new-spclaimtypeencoding.md)** <br/> |Registers a new type of claim.  <br/> |
|**[New-SPClaimTypeMapping](new-spclaimtypemapping.md)** <br/> |Creates a claim mapping rule for a security token service (STS) identity provider.  <br/> |
|**[New-SPManagedAccount](new-spmanagedaccount.md)** <br/> |Registers a new managed account.  <br/> |
|**[New-SPManagedPath](new-spmanagedpath.md)** <br/> |Creates a new managed path for the given Web application for all host header site collections.  <br/> |
|**[New-SPTrustedIdentityTokenIssuer](new-sptrustedidentitytokenissuer.md)** <br/> |Creates an identity provider in the farm.  <br/> |
|**[New-SPTrustedRootAuthority](new-sptrustedrootauthority.md)** <br/> |Creates a trusted root authority.  <br/> |
|**[New-SPTrustedServiceTokenIssuer](new-sptrustedservicetokenissuer.md)** <br/> |Creates a trust with a SharePoint farm.  <br/> |
|**[Remove-SPClaimProvider](remove-spclaimprovider.md)** <br/> |Unregisters a claim provider.  <br/> |
|**[Remove-SPClaimTypeMapping](remove-spclaimtypemapping.md)** <br/> |Deletes a claim type mapping rule for a security token service (STS) identity provider.  <br/> |
|**[Remove-SPManagedAccount](remove-spmanagedaccount.md)** <br/> |Removes a managed account registration from the farm.  <br/> |
|**[Remove-SPManagedPath](remove-spmanagedpath.md)** <br/> |Deletes the specified managed path from the specified host header or Web application.  <br/> |
|**[Remove-SPTrustedIdentityTokenIssuer](remove-sptrustedidentitytokenissuer.md)** <br/> |Deletes a security token service (STS) identity provider from the farm.  <br/> |
|**[Remove-SPTrustedRootAuthority](remove-sptrustedrootauthority.md)** <br/> |Deletes a trusted root authority.  <br/> |
|**[Remove-SPTrustedServiceTokenIssuer](remove-sptrustedservicetokenissuer.md)** <br/> |Deletes the object that represents the farm trust.  <br/> |
|**[Repair-SPManagedAccountDeployment](repair-spmanagedaccountdeployment.md)** <br/> |Repairs the local managed account credential deployment.  <br/> |
|**[Revoke-SPObjectSecurity](revoke-spobjectsecurity.md)** <br/> |Removes a security principal from a **SPObjectSecurity** object.  <br/> |
|**[Set-SPClaimProvider](set-spclaimprovider.md)** <br/> |Updates registration of a claims provider.  <br/> |
|**[Set-SPManagedAccount](set-spmanagedaccount.md)** <br/> |Configures the managed account.  <br/> |
|**[Set-SPSecurityTokenServiceConfig](set-spsecuritytokenserviceconfig.md)** <br/> |Updates the settings of the SharePoint security token service (STS) identity provider.  <br/> |
|**[Set-SPServiceApplicationSecurity](set-spserviceapplicationsecurity.md)** <br/> |Updates the **SPObjectSecurity** object for a service application.  <br/> |
|**[Set-SPTrustedIdentityTokenIssuer](set-sptrustedidentitytokenissuer.md)** <br/> |Sets the identity providers of a Web application.  <br/> |
|**[Set-SPTrustedRootAuthority](set-sptrustedrootauthority.md)** <br/> |Creates a new trusted root authority.  <br/> |
|**[Set-SPTrustedServiceTokenIssuer](set-sptrustedservicetokenissuer.md)** <br/> |Updates a trust with the farm.  <br/> |
|**[Update-SPFarmEncryptionKey](update-spfarmencryptionkey.md)** <br/> |Changes the value of the farm encryption key and, using the new key, re-encrypts all the data.  <br/> |
|**[Get-SPAuthenticationRealm](get-spauthenticationrealm.md)** <br/> |Returns the authentication realms.  <br/> |
|**[Get-SPTrustedSecurityTokenIssuer](get-sptrustedsecuritytokenissuer.md)** <br/> |Returns the trusted security token issuer object.  <br/> |
|**[New-SPAzureAccessControlServiceApplicationProxy](new-spazureaccesscontrolserviceapplicationproxy.md)** <br/> |Creates a new service application proxy group.  <br/> |
|**[New-SPTrustedSecurityTokenIssuer](new-sptrustedsecuritytokenissuer.md)** <br/> |Creates a trust between a server to server principal.  <br/> |
|**[Remove-SPTrustedSecurityTokenIssuer](remove-sptrustedsecuritytokenissuer.md)** <br/> |Removes the trusted security token service object.  <br/> |
|**[Set-SPAuthenticationRealm](set-spauthenticationrealm.md)** <br/> |Sets the authentication realm.  <br/> |
|**[Set-SPTrustedSecurityTokenIssuer](set-sptrustedsecuritytokenissuer.md)** <br/> |Sets the trusted token issuer.  <br/> |
|**[Get-SPAppPrincipal](get-spappprincipal.md)** <br/> |Displays a specific app principal object.  <br/> |
|**[Register-SPAppPrincipal](register-spappprincipal.md)** <br/> |Lets an on-premises or SharePoint Online administrator register an app principal.  <br/> |
|**[Remove-SPAppPrincipalPermission](remove-spappprincipalpermission.md)** <br/> |Removes the permissions on a specified app principal.  <br/> |
|**[Set-SPAppPrincipalPermission](set-spappprincipalpermission.md)** <br/> |Sets the permissions on a given app principal.  <br/> |
|**[Convert-SPWebApplication](convert-spwebapplication.md)** <br/> |Converts the authentication mode of a web application.  <br/> |
   

