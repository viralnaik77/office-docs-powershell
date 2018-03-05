---
title: "Set-SPSecurityTokenServiceConfig"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 2/2/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 09da9c65-598a-4068-8e1b-2f1497862e40

description: "Updates the settings of the SharePoint security token service (STS) identity provider."
---

# Set-SPSecurityTokenServiceConfig

Updates the settings of the SharePoint security token service (STS) identity provider.
  
```
Set-SPSecurityTokenServiceConfig [-ImportSigningCertificate <X509Certificate2>] <COMMON PARAMETERS>

```

## Example

------------------EXAMPLE 1------------------
  
```
Set-SPSecurityTokenServiceConfig -SigningCertificateThumbprint "2796BAE63F1801E277261BA0D77770028F20EEE4"
```

This example updates the signing certificate of the SharePoint security token service (STS) identity provider with a certificate that has been deployed in the certificate store.
  
------------------EXAMPLE 2------------------
  
```
$stsCert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2 "c:\sts.pfx","a",20
```

```
Set-SPSecurityTokenServiceConfig -ImportSigningCertificate $stsCert
```

This example imports the signing certificate for the SharePoint STS identity provider.
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
The **Set-SPSecurityTokenServiceConfig** cmdlet updates the settings of the SharePoint security token service (STS) identity provider. If a certificate file is used, the certificate must be an X509 certificate with private keys, otherwise an exception is raised. 
  
> [!NOTE]
> This cmdlet operates only with certificates that can be exported. To create a certificate which can be used in this cmdlet specify the **X509KeyStorageFlags.Exportable** bit in the **keyStorageFlags** parameter of the **x509Certificate2** object constructor. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _RevokeSigningCertificateThumbprint_ <br/> |Required  <br/> |System.String  <br/> |Revoke the signing certificate with the provided thumb print.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _FormsTokenLifetime_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the expiration time, in minutes, for tokens issued to ASP.NET Membership Provider and Role providers. The default value is 1380.  <br/> The type must be a valid integer.  <br/> |
| _ImportSigningCertificate_ <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> |Specifies the X.509 certificate object from trusted authentication provider farm.  <br/> The type must be a name of a valid X.509 certificate; for example, Certificate1.  <br/> |
| _MaxLogonTokenCacheItems_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of entries for the in-memory logon token cache. The default value is 10000 entries.  <br/> The type must be a valid integer.  <br/> |
| _MaxServiceTokenCacheItems_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of entries for the in-memory service token cache. The default value is 10000 entries.  <br/> The type must be a valid integer.  <br/> |
| _QueueSigningCertificate_ <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> |Sets the provided certificate as the queued signing certificate.  <br/> |
| _QueueSigningCertificateStoreName_ <br/> |Optional  <br/> |System.String  <br/> |The store to search in when looking up a certificate to be set as the queued signing certificate by its thumbprint. Required if **QueueSigningCertificateThumbprint** was specified.  <br/> |
| _QueueSigningCertificateThumbprint_ <br/> |Optional  <br/> |System.String  <br/> |Sets the certificate with the provided thumbprint as the queued signing certificate.  <br/> |
| _RevokeSigningCertificate_ <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> |Revokes the signing certificate that matches the provided certificate.  <br/> |
| _RevokeSigningCertificateStoreName_ <br/> |Optional  <br/> |System.String  <br/> |The store to search when looking up a certificate to be revoked by its thumbprint. Required if the **QueueSigningCertificateThumbprint** was specified.  <br/> |
| _ServiceTokenCacheExpirationWindow_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the interval, in minutes, for automatically renewing the token in the cache. The default value is 10 minutes.  <br/> The type must be a valid integer.  <br/> |
| _ServiceTokenLifetime_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the expiration time, in minutes, for the security token service cache. The default value is 15 minutes.  <br/> The type must be a valid integer.  <br/> |
| _SigningCertificateStoreName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the certificate store where the signing certificate resides. The identity store for an identity provider can be a SQL database table, an Active Directory Domain Services (AD DS), or Active Directory Lightweight Directory Service (AD LDS).  <br/> The type must be a valid identity of a signing certificate store; for example IdentityStore1.  <br/> |
| _SigningCertificateThumbprint_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the thumbrpint of the signing certificate.  <br/> The type must be a valid identity of a signing certificate; for example 2796BAE63F1801E277261BA0D77770028F20EEE4.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WindowsTokenLifetime_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the expiration time, in minutes, for tokens issued to Windows users. The default value is 1380 minutes.  <br/> The type must be a valid integer.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**QueueSigningCertificateThumbprint** <br/> |Required  <br/> |System.String  <br/> ||
|**RevokeSigningCertificateThumbprint** <br/> |Required  <br/> |System.String  <br/> ||
|**SigningCertificateThumbprint** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**FormsTokenLifetime** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**ImportSigningCertificate** <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> ||
|**MaxLogonTokenCacheItems** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**MaxServiceTokenCacheItems** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**QueueSigningCertificate** <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> ||
|**QueueSigningCertificateStoreName** <br/> |Optional  <br/> |System.String  <br/> ||
|**RevokeSigningCertificate** <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> ||
|**RevokeSigningCertificateStoreName** <br/> |Optional  <br/> |System.String  <br/> ||
|**ServiceTokenCacheExpirationWindow** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**ServiceTokenLifetime** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**SigningCertificateStoreName** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WindowsTokenLifetime** <br/> |Optional  <br/> |System.Int32  <br/> ||
   
## See also

#### 

[Get-SPSecurityTokenServiceConfig](get-spsecuritytokenserviceconfig.md)

