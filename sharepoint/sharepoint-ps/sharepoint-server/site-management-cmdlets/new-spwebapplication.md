---
title: "New-SPWebApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaeb5bed-81e7-4275-b005-aa7fc465e6d5

description: "Creates a new Web application within the local farm."
---

# New-SPWebApplication

Creates a new Web application within the local farm.
  
```
New-SPWebApplication -ApplicationPool <String> -Name <String> [-AdditionalClaimProvider <SPClaimProviderPipeBind[]>] [-AllowAnonymousAccess <SwitchParameter>] [-ApplicationPoolAccount <SPProcessAccountPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-AuthenticationMethod <String>] [-AuthenticationProvider <SPAuthenticationProviderPipeBind[]>] [-Confirm [<SwitchParameter>]] [-DatabaseCredentials <PSCredential>] [-DatabaseName <String>] [-DatabaseServer <String>] [-HostHeader <String>] [-Path <String>] [-Port <UInt32>] [-SecureSocketsLayer <SwitchParameter>] [-ServiceApplicationProxyGroup <SPServiceApplicationProxyGroupPipeBind>] [-SignInRedirectProvider <SPTrustedIdentityTokenIssuerPipeBind>] [-SignInRedirectURL <String>] [-Url <String>] [-UserSettingsProvider <SPUserSettingsProviderPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Creates a new Web application specified by the **Name** parameter. The user specified by the **DatabaseCredentials** parameter must be a member of the **dbcreator** fixed server role on the database server. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationPool** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of an application pool to use; for example, SharePoint - 1213. If an application pool with the name provided does not exist, the **ApplicationPoolAccount** parameter must be provided and a new application pool will be created. If no value is specified, the default application pool will be used.  <br/> |
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the new Web application.  <br/> |
|**AdditionalClaimProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPClaimProviderPipeBind[]  <br/> |Adds a specific claim provider to the defined Web application.  <br/> |
|**AllowAnonymousAccess** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Allows anonymous access to the Web application.  <br/> |
|**ApplicationPoolAccount** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPProcessAccountPipeBind  <br/> |Specifies the user account that this application pool will run as. Use the **Get-SPIisWebServicApplicationPool** cmdlet to use a system account.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**AuthenticationMethod** <br/> |Optional  <br/> |System.String  <br/> |Uses **Kerberos** or **NTLM** to specify the authentication method. If no value is specified, the default **NTLM** is applied.  <br/> |
|**AuthenticationProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAuthenticationProviderPipeBind[]  <br/> |Specifies the authentication provider or providers that apply to a Web application.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the Windows PowerShell **Credential** object for the database user account.  <br/> |
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the initial content database for the new Web application.  <br/> The type must be a valid database name; for example, ContentDB1. If no value is specified, a value in the format WSS_Content_\<GUID\> is auto-generated.  <br/> |
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> |Specifies the database server name. The type must be a valid database server name, in the form SQL1; where named instances are used, the format can appear as server\server. The default SQL server instance is used if a value is not provided.  <br/> |
|**HostHeader** <br/> |Optional  <br/> |System.String  <br/> |Specifies a valid URL assigned to the Web application that must correlate to the alternate access mapping configuration, in the form server_name.  <br/> When the **HostHeader** parameter is present, the value of this field is the internal URL for the Web application. The **Url** parameter is used to specify the public URL.If no value is specified, the value is left blank.  <br/> |
|**Path** <br/> |Optional  <br/> |System.String  <br/> |Specifies the physical directory for the new Web application in the virtual directories folder. The type is a valid path, in the form C:\Inutepub\wwwroot\MyWebApplication. If no value is specified, the value %wwwroot%\wss\VirtualDirectories\\<portnumber\> is applied.  <br/> |
|**Port** <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the port on which this Web application can be accessed. This can be any valid port number. If no port is specified, a nonconflicting port number is automatically generated.  <br/> > [!IMPORTANT]> If you specify a port number that has already been assigned, IIS does not start the new site until you change either the port number of the new site or the port number of the old site.           |
|**SecureSocketsLayer** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Enables Secure Sockets Layer (SSL) encryption for this Web application. If you choose to use SSL, you must add the certificate on each server by using the IIS administration tools. Until this is done, the Web application will be inaccessible from this IIS Web site.  <br/> |
|**ServiceApplicationProxyGroup** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyGroupPipeBind  <br/> |Specifies a custom service application proxy group for the Web application to use. The Web application will use the proxies in this proxy group to connect to service applications. If this parameter is not specified, the default proxy group for the farm is used.  <br/> |
|**SignInRedirectProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> |Sets the sign-in redirect URL to point to the URL that is defined in the specified authentication provider.  <br/> |
|**SignInRedirectURL** <br/> |Optional  <br/> |System.String  <br/> |Specifies the sign-in redirect URL for the Web application.  <br/> |
|**Url** <br/> |Optional  <br/> |System.String  <br/> |Specifies the load-balanced URL for the Web application.  <br/> |
|**UserSettingsProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUserSettingsProviderPipeBind  <br/> |Provides access to external user settings provider.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationPool** <br/> |Required  <br/> |System.String  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**AdditionalClaimProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPClaimProviderPipeBind[]  <br/> ||
|**AllowAnonymousAccess** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ApplicationPoolAccount** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPProcessAccountPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**AuthenticationMethod** <br/> |Optional  <br/> |System.String  <br/> ||
|**AuthenticationProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAuthenticationProviderPipeBind[]  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**HostHeader** <br/> |Optional  <br/> |System.String  <br/> ||
|**Path** <br/> |Optional  <br/> |System.String  <br/> ||
|**Port** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**SecureSocketsLayer** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ServiceApplicationProxyGroup** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyGroupPipeBind  <br/> ||
|**SignInRedirectProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> ||
|**SignInRedirectURL** <br/> |Optional  <br/> |System.String  <br/> ||
|**Url** <br/> |Optional  <br/> |System.String  <br/> ||
|**UserSettingsProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUserSettingsProviderPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
$ap = New-SPAuthenticationProvider
```

```
New-SPWebApplication -Name "Contoso Internet Site" -Port 443 -HostHeader sharepoint.contoso.com -URL "https://www.contoso.com" -ApplicationPool "ContosoAppPool" -ApplicationPoolAccount (Get-SPManagedAccount "DOMAIN\jdoe") -AuthenticationProvider $ap -SecureSocketsLayer
```

This example creates a new Web application by using an internal host header of  `sharepoint.contoso.com` and a public URL of  `https://www.contoso.com`.
  
## See also

#### 

[Get-SPWebApplication](get-spwebapplication.md)
  
[Set-SPWebApplication](set-spwebapplication.md)
  
[Get-SPWebApplication](get-spwebapplication.md)

