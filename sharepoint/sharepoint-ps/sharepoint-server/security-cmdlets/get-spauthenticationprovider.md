---
title: "Get-SPAuthenticationProvider"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6d779f-51b3-4da0-8408-591393048168

description: "Returns an authentication provider."
---

# Get-SPAuthenticationProvider

Returns an authentication provider.
  
```
Get-SPAuthenticationProvider [[-Identity] <SPAuthenticationProviderPipeBind>] [-WebApplication] <SPWebApplicationPipeBind> [-Zone] <Default | Intranet | Internet | Custom | Extranet> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPAuthenticationProvider** cmdlet returns an authentication provider on a specified Web application zone. The following are the standard authentication providers available for SharePoint 2010 Products: **NTLM**, **Classic NTLM**, **Negotiate**, and **Classic Negotiate**.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAuthenticationProviderPipeBind  <br/> |Specifies the authentication provider to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint authentication provider (for example, NTLM); or an instance of a valid **SPAuthenticationProvider** object.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Returns the content databases for the specified Web application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of SharePoint Web application (for example, MyOfficeApp1); or an instance of a valid **SPWebApplication** object.  <br/> |
|**Zone** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> |Specifies the Web application zone or zones for which to return the authentication provider.  <br/> The type must be any one of the valid zones: Default, Intranet, Internet, Extranet, or Custom.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAuthenticationProviderPipeBind  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**Zone** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-----------------EXAMPLE 1-----------------
  
```
New-SPWebApplication http://sharepointonline.com -AuthenticationProvider (Get-SPAuthenticationProvider "LiveID STS")
```

This example registers the  `LiveID STS` authentication provider for the new Web application. 
  
-----------------EXAMPLE 2-----------------
  
```
New-SPWebApplication http://contoso.com -AuthenticationProvider (New-SPAuthenticationProvider -ASPNetMembershipProvider "myMembershipProvider" -ASPNetRoleProvider "myRoleProvider")
```

This example registers  `ASPNet` for the new Web application. Note that ASPNET memberships are not persisted and must be re-created every use. 
  
-----------------EXAMPLE 3-----------------
  
```
New-SPWebApplication http://contoso.com -AuthenticationProvider (Get-SPAuthenticationProvider "NTLM")
```

This example registers the  `NTLM` authentication provider for the new Web application. This command is equivalent to the command  `New-SPWebApplication http://contoso.com`;  `NTLM` is default authentication provider. 
  
-----------------EXAMPLE 4-----------------
  
```
$ip = @( (Get-SPAuthenticationProvider "LiveID STS"), (New-SPAuthenticationProvider -ASPNetMembershipProvider "myMembershipProvider" -ASPNetRoleProvider "myRoleProvider"), (Get-SPAuthenticationProvider "NTLM")) )New-SPWebApplication http://contoso.com -AuthenticationProvider $ip
```

This example registers the  `NTLM`,  `ASPNet`, and  `LiveID STS` authentication providers for the new Web application. 
  
-----------------EXAMPLE 5-----------------
  
```
New-SPWebApplication http://contoso.com -AuthenticationProvider (Get-SPAuthenticationProvider "Legacy NTLM")
```

This example registers the  `Legacy NTLM` authentication provider for the new Web application. 
  
## See also

#### 

[New-SPAuthenticationProvider](new-spauthenticationprovider.md)

