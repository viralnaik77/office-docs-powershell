---
title: "Set-SPTrustedSecurityTokenIssuer"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/7/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5f969a76-adc7-47c6-84f4-624c349529eb

description: "Sets the trusted token issuer."
---

# Set-SPTrustedSecurityTokenIssuer

Sets the trusted token issuer.
  
```
Set-SPTrustedSecurityTokenIssuer [-Identity] <SPTrustedSecurityTokenServicePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Description <String>] [-IsTrustBroker <SwitchParameter>] [-MetadataEndPoint <Uri>] [-RegisteredIssuerName <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **Set-SPTrustedSecurityTokenIssuer** cmdlet to set the trusted token issuer. 
  
To set the certificate successfully, all of the required parameters must be specified.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedSecurityTokenServicePipeBind  <br/> |Specifies the id of the **SPTrustedSecurityTokenIssuer** object to be set.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Certificate** <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> |Specifies the X509Certificate object that represents the public key of the signing certificate of the security token issuer.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Description** <br/> |Optional  <br/> |System.String  <br/> |Specifies the description of the issuer.  <br/> |
|**IsTrustBroker** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether the trust is established with a self-issuer partner app (that is, Exchange Server 2010 or Exchange Server 2007 or Skype for Business).  <br/> |
|**MetadataEndPoint** <br/> |Optional  <br/> |System.Uri  <br/> |Specifies the URI for the metadata endpoint of the issuer.  <br/> |
|**RegisteredIssuerName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the Registered Issuer Name when not using the metadata endpoint.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedSecurityTokenServicePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Certificate** <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Description** <br/> |Optional  <br/> |System.String  <br/> ||
|**IsTrustBroker** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**MetadataEndPoint** <br/> |Optional  <br/> |System.Uri  <br/> ||
|**RegisteredIssuerName** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------EXAMPLE---------
  
```
$a=Get-SPTrustedSecurityTokenIssuer
```

```
Set-SPTrustedSecurityTokenIssuer -Identity $a -MetadataEndpoint https://<webappurl/>/_layouts/15/metadata/json/1/
```

This example sets the metadata endpoint of the url for the self-issue.
  
## See also

#### 

[Get-SPTrustedSecurityTokenIssuer](get-sptrustedsecuritytokenissuer.md)
  
[New-SPTrustedSecurityTokenIssuer](new-sptrustedsecuritytokenissuer.md)
  
[Remove-SPTrustedSecurityTokenIssuer](remove-sptrustedsecuritytokenissuer.md)

