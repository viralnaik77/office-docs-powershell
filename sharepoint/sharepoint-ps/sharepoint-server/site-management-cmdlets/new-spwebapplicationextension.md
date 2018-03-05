---
title: "New-SPWebApplicationExtension"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c407f36-6e3d-4213-bdb9-8298fa0c761c

description: "Creates a new zone instance for the Web application."
---

# New-SPWebApplicationExtension

Creates a new zone instance for the Web application.
  
```
New-SPWebApplicationExtension [-Identity] <SPWebApplicationPipeBind> -Name <String> -Zone <Default | Intranet | Internet | Custom | Extranet> [-AdditionalClaimProvider <SPClaimProviderPipeBind[]>] [-AllowAnonymousAccess <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>] [-AuthenticationMethod <String>] [-AuthenticationProvider <SPAuthenticationProviderPipeBind[]>] [-Confirm [<SwitchParameter>]] [-HostHeader <String>] [-Path <String>] [-Port <UInt32>] [-SecureSocketsLayer <SwitchParameter>] [-SignInRedirectProvider <SPTrustedIdentityTokenIssuerPipeBind>] [-SignInRedirectURL <String>] [-Url <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **New-SPWebApplicationExtension** cmdlet creates a new zone instance for the Web application. This is also known as extending a Web application and allows alternate permissions to be configured for the same content that is available in the existing Web application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the Web application to extend.  <br/> |
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the new IIS Web site in the Web application.  <br/> |
|**Zone** <br/> |Required  <br/> |System.String  <br/> |Specifies one of the five zones with which the internal URL of this new extension is to be associated. This zone cannot already be in use..  <br/> The type must be any one of the following values: **Default**, **Intranet**, **Internet**, **Extranet**, or **Custom** <br/> |
|**AdditionalClaimProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPClaimProviderPipeBind[]  <br/> |Adds a specific claim provider to the defined Web application.  <br/> |
|**AllowAnonymousAccess** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Allows anonymous access to the Web application zone.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**AuthenticationMethod** <br/> |Optional  <br/> |String  <br/> |Uses **Kerberos** or **NTLM** to specify the authentication method.  <br/> |
|**AuthenticationProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAuthenticationProviderPipeBind[]  <br/> |Specifies the authentication provider(s) that applies to a Web apllication.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**HostHeader** <br/> |Optional  <br/> |System.String  <br/> |Specifies a valid URL assigned to the Web application by that must correlate to the alternate access mapping configuration, in the form http://server_name.  <br/> When the **HostHeader** parameter is present, the value of this field is the internal URL for the Web application. The **Url** parameter is used to specify the public URL.  <br/> |
|**Path** <br/> |Optional  <br/> |System.String  <br/> |Specifies the physical directory for the new Web site (in the virtual directories folder). The type is a valid path, in the form C:\Inetpub\wwwroot\MyWebApplication.  <br/> |
|**Port** <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the application port. Can be any valid port number.  <br/> If no port is specified, a nonconflicting port number is automatically generated.  <br/> > [!IMPORTANT]> If you specify a port number that is already assigned, IIS does not start the new site until you change either the port number of the new site or the port number of the old site.           |
|**SecureSocketsLayer** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Enables Secure Sockets Layer (SSL) encryption for this Web application. If you use SSL, you must add the certificate on each server by using the IIS administration tools. Until this is done, the Web application is inaccessible from this IIS Web site.  <br/> |
|**SignInRedirectProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> |Sets the sign-in redirect URL to point to the URL that is defined in the specified authentication provider.  <br/> |
|**SignInRedirectURL** <br/> |Optional  <br/> |System.String  <br/> |Specifies the sign-in redirect URL for the Web application.  <br/> |
|**Url** <br/> |Optional  <br/> |System.String  <br/> |Specifies the load-balanced URL for the Web application zone.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**Zone** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> ||
|**AdditionalClaimProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPClaimProviderPipeBind[]  <br/> ||
|**AllowAnonymousAccess** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**AuthenticationMethod** <br/> |Optional  <br/> |System.String  <br/> ||
|**AuthenticationProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAuthenticationProviderPipeBind[]  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**HostHeader** <br/> |Optional  <br/> |System.String  <br/> ||
|**Path** <br/> |Optional  <br/> |System.String  <br/> ||
|**Port** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**SecureSocketsLayer** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SignInRedirectProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> ||
|**SignInRedirectURL** <br/> |Optional  <br/> |System.String  <br/> ||
|**Url** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
Get-SPWebApplication http://sitename | New-SPWebApplicationExtension -Name "ExtranetSite" -SecureSocketsLayer -Zone "Extranet" -URL "https://extranet.sitename.com"
```

This example extends the given Web application at  `http://sitename` to the  `Extranet` zone for SSL use. 
  
## See also

#### 

[Get-SPWebApplication](get-spwebapplication.md)
  
[Set-SPWebApplication](set-spwebapplication.md)

