---
title: "Set-SPTrustedRootAuthority"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/7/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4a1bc19a-ae07-4f29-ba6c-e9bad5daed9e

description: "Creates a new trusted root authority."
---

# Set-SPTrustedRootAuthority

Creates a new trusted root authority.
  
```
Set-SPTrustedRootAuthority [-Identity] <SPTrustedRootAuthorityPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Certificate <X509Certificate2>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Set-SPTrustedRootAuthority** cmdlet creates a new trusted root authority. If a certificate file is used, the certificate must be an X509 certificate with private keys, otherwise an exception is raised. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedRootAuthorityPipeBind  <br/> |Specifies the trusted root authority to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a trusted root authority (for example, WFEFarm1); or an instance of a valid **SPTrustedRootAuthority** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Certificate** <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> |Specifies the X.509 certificate of the trusted root authority.  <br/> The type must be a name of a valid X.509 certificate; for example, Certificate1.  <br/> |
|**MetadataEndPoint** <br/> |Optional  <br/> |System.Uri  <br/> |Specifies the URI for the metadata endpoint of the trusted provider.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedRootAuthorityPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Certificate** <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**MetadataEndPoint** <br/> |Optional  <br/> |System.Uri  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$cert = Get-PfxCertificate C:\LiveIDSigningCert.pfx
Get - SPTrustedRootAuthority -Name "WFEFarm1" | Set- SPTrustedRootAuthority -Certificate $cert
```

This example updates the certificate of the trusted root authority  `WFEFarm1`.
  
## See also

#### 

[Remove-SPTrustedRootAuthority](remove-sptrustedrootauthority.md)
  
[New-SPTrustedRootAuthority](new-sptrustedrootauthority.md)
  
[Get-SPTrustedRootAuthority](get-sptrustedrootauthority.md)

