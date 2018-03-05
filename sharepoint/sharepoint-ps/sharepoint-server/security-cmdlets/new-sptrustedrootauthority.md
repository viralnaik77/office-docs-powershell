---
title: "New-SPTrustedRootAuthority"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 25458530-4f0d-491c-80d3-61b8f1f0dd7e

description: "Creates a trusted root authority."
---

# New-SPTrustedRootAuthority

Creates a trusted root authority.
  
```
New-SPTrustedRootAuthority [-Name] <String> -Certificate <X509Certificate2> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **New-SPTrustedRootAuthority** cmdlet creates a trusted root authority. If a certificate file is used, it must have only one X509 certificate without private keys, otherwise an exception is raised. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the trusted root authority to create.  <br/> The value must be a valid name of a trusted root authority; for example, WFEFarm1.  <br/> |
|**Certificate** <br/> |Required  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> |Specifies the X.509 certificate of the trusted root authority.  <br/> The value must be a name of a valid X.509 certificate; for example, Certificate1.  <br/> |
|**MetadataEndPoint** <br/> |Required  <br/> |System.Uri  <br/> |Specifies the Uri of the metadata endpoint.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**Certificate** <br/> |Required  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> ||
|**MetadataEndPoint** <br/> |Required  <br/> |System.Uri  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$cert = Get-PfxCertificate C:\LiveIDSigningCert.pfx
```

```
New-SPTrustedRootAuthority -Name "WFEFarm1" -Certificate $cert
```

This example creates a new trusted root authority,  `WFEFarm1`.
  
## See also

#### 

[Get-SPTrustedRootAuthority](get-sptrustedrootauthority.md)
  
[Set-SPTrustedRootAuthority](set-sptrustedrootauthority.md)
  
[Remove-SPTrustedRootAuthority](remove-sptrustedrootauthority.md)

