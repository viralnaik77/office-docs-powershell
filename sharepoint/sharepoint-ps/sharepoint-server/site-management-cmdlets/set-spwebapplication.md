---
title: "Set-SPWebApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 1/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0dd61e54-0e77-44b3-86c5-fabc128efa7b

description: "Configures the specified Web application."
---

# Set-SPWebApplication

Configures the specified Web application.
  
```
Set-SPWebApplication [-DefaultQuotaTemplate <String>] [-DefaultTimeZone <Int32>] [-ServiceApplicationProxyGroup <SPServiceApplicationProxyGroupPipeBind>] <COMMON PARAMETERS>

```

## Example

------------------EXAMPLE-----------------------
  
```
Get-SPWebApplication http://somesite | Set-SPWebApplication -OutgoingEmailAddress "davlon@contoso.com" - AllowAnonymousAccess
```

This example sets the  `OutgoingEmailAddress` for the given Web application as  `davlon@contoso.com` and enables anonymous access. 
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
The **Set-SPWebApplication** cmdlet configures the Web application specified by the **Identity** parameter. For any settings that are zone-specific (for the **Zone** parameter set), the zone to configure must be provided. The provided zone must already exist. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the name or URL of the Web application.  <br/> The type must be a valid name, in the form WebApplication-1212, or URL, in the form http://server_name/WebApplicaiton-1212.  <br/> |
| _SMTPServer_ <br/> |Required  <br/> |System.String  <br/> |Specifies the new outbound SMTP server that this Web application will use.  <br/> |
| _Zone_ <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> |When configuring zone-specific settings, the zone to configure must be specified. This zone must already exist.  <br/> The type must be any one of the following values: **Default**, **Intranet**, **Internet**, **Extranet**, or **Custom**.  <br/> |
| _AdditionalClaimProvider_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPClaimProviderPipeBind[]  <br/> |Adds a specific claim provider to the defined Web application.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _AuthenticationMethod_ <br/> |Optional  <br/> |System.String  <br/> |Use to set a Web application to classic Windows authentication. The valid values are NTLM or Kerberos.  <br/> |
| _AuthenticationProvider_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAuthenticationProviderPipeBind[]  <br/> |Defines the authentication provider(s) that applies to the Web application.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DefaultQuotaTemplate_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the new default site quota template for this Web application.  <br/> |
| _DefaultTimeZone_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the default time zone for new site collections in this Web application.  <br/> |
| _DisableSMTPEncryption_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether to turn on or off SMTP Encryption.  <br/> The default value is false.  <br/> |
| _Force_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Suppresses confirmation messages involved in settings for a Web application.  <br/> |
| _NotProvisionGlobally_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Skips the Web application provision process.  <br/> |
| _OutgoingEmailAddress_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the new outgoing e-mail address for e-mail messages sent from this Web application. The type must be a valid address; for example, someone@example.com.  <br/> |
| _ReplyToEmailAddress_ <br/> |Optional  <br/> |System.String  <br/> |Configures the reply e-mail address.  <br/> The type must be a valid address; for example, someone@example.com.  <br/> |
| _ServiceApplicationProxyGroup_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyGroupPipeBind  <br/> |Specifies a custom service application proxy group for the Web application to use. The Web application will use the proxies in this proxy group to connect to service applications. If this parameter is not specified, the farm's default proxy group is used.  <br/> |
| _SignInRedirectProvider_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> |Sets the sign-in redirect URL to point to the URL that is defined in the specified authentication provider.  <br/> |
| _SignInRedirectURL_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the sign-in redirect URL for the Web application.  <br/> |
| _SMTPServerPort_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies a SMTP port value.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**HostHeader** <br/> |Optional  <br/> |System.String  <br/> |Specifies a valid URL assigned to the Web application that must correlate to the alternate access mapping configuration; for example, http://server_name. When the **HostHeader** parameter is present, the value of this field is the internal URL for the Web application. The **Url** parameter is used to specify the public URL.  <br/> |
|**SecureSocketsLayer** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Enables Secure Sockets Layer (SSL) encryption for this Web application. If you use SSL, you must add the certificate on each server by using the IIS administration tools. Until you add the certificates, the Web application is inaccessible from this IIS Web site.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**SMTPServer** <br/> |Required  <br/> |System.String  <br/> ||
|**Zone** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> ||
|**AdditionalClaimProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPClaimProviderPipeBind[]  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**AuthenticationMethod** <br/> |Optional  <br/> |System.String  <br/> ||
|**AuthenticationProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAuthenticationProviderPipeBind[]  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultQuotaTemplate** <br/> |Optional  <br/> |System.String  <br/> ||
|**DefaultTimeZone** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**OutgoingEmailAddress** <br/> |Optional  <br/> |System.String  <br/> ||
|**ReplyToEmailAddress** <br/> |Optional  <br/> |System.String  <br/> ||
|**ServiceApplicationProxyGroup** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyGroupPipeBind  <br/> ||
|**SignInRedirectProvider** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> ||
|**SignInRedirectURL** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPWebApplication](get-spwebapplication.md)
  
[New-SPWebApplication](new-spwebapplication.md)
  
[Remove-SPWebApplication](remove-spwebapplication.md)

