---
title: "Set-SPServiceHostConfig"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea27e2c6-7913-4f0a-92ec-33ca6e972a57

description: "Configures one or more common settings for all Web services."
---

# Set-SPServiceHostConfig

Configures one or more common settings for all Web services.
  
```
Set-SPServiceHostConfig [-Identity] <SPIisWebServiceSettings> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-HttpPort <Int32>] [-HttpsPort <Int32>] [-ImportSslCertificate <X509Certificate2>] [-NetTcpPort <Int32>] [-NoWait <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Set- SPServiceHostConfig** cmdlet configures one or more common settings for all Web services. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPIisWebServiceSettings  <br/> |Specifies the identity of the Web service application to configure.  <br/> |
|**SslCertificateThumbprint** <br/> |Required  <br/> |System.String  <br/> |Specifies the thumbprint of the SSL certificate to retrieve for secure protocols.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**HttpPort** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the new port for the Web service.  <br/> |
|**HttpsPort** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the new secure port for the Web service.  <br/> |
|**ImportSslCertificate** <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> |Specifies the SSL Certificate to use for secure protocols.  <br/> |
|**NetTcpPort** <br/> |Optional  <br/> |System.Int32  <br/> |Sets the TCP port for the Web service.  <br/> |
|**NoWait** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |For more information, see TechNet.  <br/> |
|**SslCertificateStoreName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the thumbprint of the SSL certificate to retrieve for secure protocols.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPIisWebServiceSettings  <br/> ||
|**SslCertificateThumbprint** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**HttpPort** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**HttpsPort** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**ImportSslCertificate** <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> ||
|**NetTcpPort** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**NoWait** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SslCertificateStoreName** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
Set-SPServiceHostConfig -Port 12345
```

This example sets the HTTP port for the Web services. 
  
## See also

#### 

[Get-SPServiceHostConfig](get-spservicehostconfig.md)

