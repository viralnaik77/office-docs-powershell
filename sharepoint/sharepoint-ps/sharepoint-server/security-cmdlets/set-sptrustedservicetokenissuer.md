---
title: "Set-SPTrustedServiceTokenIssuer"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/7/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea727c90-7344-4c25-b3b7-c5b422ef0833
description: "Updates a trust with the farm."
---

# Set-SPTrustedServiceTokenIssuer

Updates a trust with the farm.
  
```
Set-SPTrustedServiceTokenIssuer [-Identity] <SPTrustedServiceTokenIssuerPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Certificate <X509Certificate2>] [-Confirm [<SwitchParameter>]] [-Description <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Set-SPTrustedServiceTokenIssuer** cmdlet updates a trust with a SharePoint farm. If a certificate file is used, it must have only one X509 certificate without private keys, otherwise an exception is raised. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedServiceTokenIssuerPipeBind  <br/> |Specifies the trusted service token issuer to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a trusted service token issuer (for example, WFEFarm1); or an instance of a valid **SPTrustedRootAuthority** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.  <br/> |
|**Certificate** <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> |Specifies the X.509 certificate object from trusted authentication provider farm.  <br/> The type must be a name of a valid X.509 certificate; for example, Certificate1.  <br/> |
|**Description** <br/> |Optional  <br/> |System.String  <br/> |Specifies a description for the trust.  <br/> The type must be a valid string; for example, WFE Farm Trust1.  <br/> |
|**MetadataEndPoint** <br/> |Optional  <br/> |System.Uri  <br/> |Specifies the URI for the metadata endpoint of the trusted provider.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedServiceTokenIssuerPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Certificate** <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Description** <br/> |Optional  <br/> |System.String  <br/> ||
|**MetadataEndPoint** <br/> |Optional  <br/> |System.Uri  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1------------------
  
```
$cert = Get-PfxCertificate C:\LiveIDSigningCert.pfxSet-SPTrustedServiceTokenIssuer "WFEFarm1" - Description "WFE Farm 1" - ImportTrustCertificate $cert
```

This example updates a SharePoint Farm trust using the trust certificate from a file.
  
------------------EXAMPLE 2------------------
  
```
Set-SPTrustedServiceTokenIssuer "WFEFarm1" - Description "WFE Farm 1" -FederationMetadataUrl "https://liveid.com/STS/2007/03/fedmetadata.xml"
```

This example updates a SharePoint farm trust using the trust certificate from the federation metadata endpoint URL.
  
## See also

#### 

[Get-SPTrustedServiceTokenIssuer](get-sptrustedservicetokenissuer.md)
  
[New-SPTrustedServiceTokenIssuer](new-sptrustedservicetokenissuer.md)
  
[Remove-SPTrustedServiceTokenIssuer](remove-sptrustedservicetokenissuer.md)

