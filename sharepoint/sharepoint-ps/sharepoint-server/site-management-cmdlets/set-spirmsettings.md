---
title: "Set-SPIRMSettings"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5451adc2-3e71-403d-b7dc-5c1ecacc7195

description: "Sets the Information Rights Management (IRM) settings."
---

# Set-SPIRMSettings

Sets the Information Rights Management (IRM) settings.
  
```
Set-SPIRMSettings [-UseActiveDirectoryDiscovery <SwitchParameter>] <COMMON PARAMETERS>

```

## Example

--------------EXAMPLE 1------------ 
  
```
Set-SPIRMSettings -IrmEnabled -UseActiveDirectoryDiscovery
```

This example enables IRM for the farm and configures it to use the default RMS server configured in Active Directory.
  
--------------EXAMPLE 2------------ 
  
```
Set-SPIRMSettings -IrmEnabled -CertificateServerUrl http://myrmsserver
```

This example enables IRM for the farm and specifies the URL of the RMS server to use.
  
--------------EXAMPLE 3------------ 
  
```
site = Get-SPSite http://myspserver
```

```
$subscription = $site.SiteSubscription
```

```
Set-SPIRMSettings -SiteSubscription $subscription -IrmEnabled -CertificateServerUrl http://myrmsserver
```

This example enables IRM for the specified tenant and specifies the URL of the RMS server to use.
  
--------------EXAMPLE 4------------ 
  
```
Set-SPIRMSettings -IrmEnabled:$false
```

This example disables IRM for the farm.
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
Use the **Set-SPIRMSettings** cmdlet to set the Information Rights Management (IRM) settings for the tenant. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _CertificateServerUrl_ <br/> |Required  <br/> |System.Uri  <br/> |Specifies the address of the RMS certificate server to use for the tenant.  <br/> |
| _IrmEnabled_ <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether or not IRM is enabled in the tenant.  <br/> The default value is false.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CertificatePassword_ <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the password to access the Service Authentication Certificate. This password is required in order to install the certificate in the machine certificate store.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _ServiceAuthenticationCertificate_ <br/> |Optional  <br/> |System.Security.Cryptography.X509Certificates.X509Certificate2  <br/> |Specifies the service authentication certificate.  <br/> If the parameter is specified and not null, the authentication certificate is used when connecting from this farm to the RMS server. If the parameter is not specified, the local farm connects to RMS server using integrated windows authentication.  <br/> |
| _SubscriptionScopeSettingsEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether or not IRM can be configured at the site subscription scope.  <br/> Site subscriptions can only configure custom IRM settings if IRM is enabled at the Farm scope.  <br/> |
| _UseActiveDirectoryDiscovery_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether or not the RMS service should be used for discovery that will determine the address of the RMS server in the domain.  <br/> |
| _UseOauth_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether OAuth should be used.  <br/> The valid values are **True** and **False**.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Get-SPIRMSettings](get-spirmsettings.md)

