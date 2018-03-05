---
title: "New-SPAuthenticationProvider"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c1056674-30b6-4c9c-bfc7-a2d336064b62

description: "Creates a new authentication provider in the farm."
---

# New-SPAuthenticationProvider

Creates a new authentication provider in the farm.
  
```
New-SPAuthenticationProvider [-AllowAnonymous <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>] [-DisableKerberos <SwitchParameter>] [-UseBasicAuthentication <SwitchParameter>] [-UseWindowsIntegratedAuthentication <SwitchParameter>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **New-SPAuthenticationProvider** cmdlet creates a new authentication provider in the farm. 
  
--NTLM, Classic NTLM, Negotiate, and Classic Negotiate can be set only in a web application.
  
--For ASP.NET Membership Provider or Role providers, no objects are persisted. The object is created and used for setting this type of Authentication provider in a web application.
  
--For STS Authentication providers, an object is created and persisted in the **SPFarm** object. 
  
You cannot use classic NTLM with any claims-based authentication type.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ASPNETMembershipProvider** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the membership provider.  <br/> The value must be a valid name of an ASP.NET membership provider; for example, myMembershipProvider.  <br/> |
|**ASPNETRoleProviderName** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the role provider.  <br/> The value must be a valid name of an ASP.NET role provider; for example, myRoleProvider.  <br/> |
|**TrustedIdentityTokenIssuer** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> |Specifies the identity of the authentication provider.  <br/> The value must be in one of the following forms:  <br/> --A valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh  <br/> --A valid name of a TrustedIdentityTokenIssuer (for example, myRoleProvider)  <br/> --An instance of a valid **SPTrustedIdentityTokenIssuer** object  <br/> |
|**AllowAnonymous** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether the web application allows anonymous access.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**DisableKerberos** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether the web application disables Kerberos authentication.  <br/> |
|**UseBasicAuthentication** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether the web application uses Basic authentication.  <br/> |
|**UseWindowsIntegratedAuthentication** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether the web application uses Integrated Windows authentication.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ASPNETMembershipProvider** <br/> |Required  <br/> |System.String  <br/> ||
|**ASPNETRoleProviderName** <br/> |Required  <br/> |System.String  <br/> ||
|**TrustedIdentityTokenIssuer** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> ||
|**AllowAnonymous** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**DisableKerberos** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**UseBasicAuthentication** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**UseWindowsIntegratedAuthentication** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------------------EXAMPLE1------------------
  
```
$ap = New - SPAuthenticationProvider -UseWindowsIntegratedAuthentication
```

```
Set-SPWebApplication -Name "Claims Windows Web App" -ApplicationPool "Claims App Pool" -ApplicationPoolAccount "redmond\appool" -Url http://<servername> -Port 80 -AuthenticationProvider $ap
```

This example creates a Windows claims authentication provider.
  
---------------------------EXAMPLE2------------------
  
```
$ap = New-SPAuthenticationProvider -ASPNETMembershipProvider "membership" -ASPNETRoleProviderName "rolemanager"
```

```
Set-SPWebApplication -Name "Claims Windows Web App" -ApplicationPool "Claims App Pool" -ApplicationPoolAccount "redmond\appool" -Url http://<servername> -Port 80 -AuthenticationProvider $ap
```

This example creates an authentication provider that is based on the ASP.NET membership role provider.
  
---------------------------EXAMPLE3------------------
  
```
$ap = New - SPAuthenticationProvider -TrustedIdentityTokenIssuer | Get-SPTrustedIdentityTokenIssuer "LiveIDSTS"
```

```
Set-SPWebApplication -Name "Claims Windows Web App" -ApplicationPool "Claims App Pool" -ApplicationPoolAccount "redmond\appool" -Url http://<servername> -Port 80 -AuthenticationProvider $ap
```

This example creates a trusted token issuer authentication provider.
  

