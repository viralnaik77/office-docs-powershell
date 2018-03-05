---
title: "New-SPTrustedSecurityTokenIssuer"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/7/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ab7aac9-4c9a-4cba-8dd6-ffead217c2fa

description: "Creates a trust between a server to server principal."
---

# New-SPTrustedSecurityTokenIssuer

Creates a trust between a server to server principal.
  
```
New-SPTrustedSecurityTokenIssuer [-Name] <String> -Certificate <X509Certificate2> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Description <String>] [-IsTrustBroker <SwitchParameter>] [-RegisteredIssuerName <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **New-SPTrustedSecurityTokenIssuer** cmdlet to establish a trust between a server to server principal. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the issuer.  <br/> |
|**Certificate** <br/> |Required  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> |Specifies the X509Certificate object that represents the public key of the signing certificate of the security token issuer.  <br/> |
|**MetadataEndPoint** <br/> |Required  <br/> |System.Uri  <br/> |Specifies the URI for the metadata endpoint of the issuer.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Description** <br/> |Optional  <br/> |System.String  <br/> |Specifies the description of the issuer.  <br/> |
|**IsTrustBroker** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether the trust is established with a self-issuer partner app (that is, Exchange Server 2010 or Exchange Server 2007 or Skype for Business).  <br/> |
|**RegisteredIssuerName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the registered token issuer instead of using metadata endpoint.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**Certificate** <br/> |Required  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> ||
|**MetadataEndPoint** <br/> |Required  <br/> |System.Uri  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Description** <br/> |Optional  <br/> |System.String  <br/> ||
|**IsTrustBroker** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**RegisteredIssuerName** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------EXAMPLE----------- 
  
```
New-SPTrustedSecurityTokenIssuer -Name "SPFarmA" -MetadataEndPoint https://mysite/my/_layouts/metadata/test/1/ -isSelfIssuer "false"
```

This example creates a new trusted security token named SPFarmA.
  
## See also

#### 

[Get-SPTrustedSecurityTokenIssuer](get-sptrustedsecuritytokenissuer.md)
  
[Remove-SPTrustedSecurityTokenIssuer](remove-sptrustedsecuritytokenissuer.md)
  
[Set-SPTrustedSecurityTokenIssuer](set-sptrustedsecuritytokenissuer.md)

