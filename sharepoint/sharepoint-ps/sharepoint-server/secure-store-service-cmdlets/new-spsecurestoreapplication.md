---
title: "New-SPSecureStoreApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 71aa37f1-2a15-49bc-9427-64f9a10e6d42

description: "Creates a new Secure Store application."
---

# New-SPSecureStoreApplication

Creates a new Secure Store application.
  
```
New-SPSecureStoreApplication -Fields <TargetApplicationField[]> -ServiceContext <SPServiceContextPipeBind> -TargetApplication <TargetApplication> [-Administrator <SPClaim[]>] [-AssignmentCollection <SPAssignmentCollection>] [-CredentialsOwnerGroup <SPClaim[]>] [-TicketRedeemer <SPClaim[]>]
```

## Detailed Description

The **New-SPSecureStoreApplication** cmdlet creates a new Secure Store application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context for the target application.  <br/> |
|**TargetApplication** <br/> |Required  <br/> |Microsoft.Office.SecureStoreService.Server.TargetApplication  <br/> |Specifies information about the target application. For example, the **TargetApplication** object includes data values for application name, display name, contact info, enable ticketing flag, and URL address to set the credential. The schema for the **TargetApplication** object is defined in the **ISecureSToreProviderExtended** interface that exposes the target application metadata.  <br/> |
|**Administrator** <br/> |Optional  <br/> |Microsoft.SharePoint.SPClaim[]  <br/> |Specifies the administrator of the new Secure Store application.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CredentialsOwnerGroup** <br/> |Optional  <br/> |Microsoft.SharePoint.SPClaim[]  <br/> |Specifies the claims object for the groups that own the group credentials.  <br/> |
|**Fields** <br/> |Optional  <br/> |Microsoft.Office.SecureStoreService.Server.TargetApplicationField[]  <br/> |Specifies the field information for the application. The default fields are username and password.  <br/> |
|**TicketRedeemer** <br/> |Optional  <br/> |Microsoft.SharePoint.SPClaim[]  <br/> |Specifies the ticket redeemer claim value.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Fields** <br/> |Required  <br/> |Microsoft.Office.SecureStoreService.Server.TargetApplicationField[]  <br/> ||
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**TargetApplication** <br/> |Required  <br/> |Microsoft.Office.SecureStoreService.Server.TargetApplication  <br/> ||
|**Administrator** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim[]  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CredentialsOwnerGroup** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim[]  <br/> ||
|**TicketRedeemer** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim[]  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$usernameField = New-SPSecureStoreApplicationField -Name "UserName" -Type WindowsUserName -Masked:$false
$passwordField = New-SPSecureStoreApplicationField -Name "Password" -Type WindowsPassword -Masked:$true
$fields = $usernameField,$passwordField
$userClaim = New-SPClaimsPrincipal -Identity "CONTOSO\janedoe" -IdentityType WindowsSamAccountName
$contosoTargetApp = New-SPSecureStoreTargetApplication -Name "ContosoTargetApplication" -FriendlyName "Contoso Target Application" -ApplicationType Group
New-SPSecureStoreApplication -ServiceContext http://contoso -TargetApplication $contosoTargetApp -Fields $fields -Administrator $claimUser
```

This example creates a new group target application  `ContosoTargetApplication`, and then a new application for that target application. This new application has two fields;  `UserName` of type  `WindowsUserName`, and  `Password` of type  `WindowsPassword`. The user with identity  `janedoe` on the  `CONTOSO` domain is set as the target application administrator. 
  
## See also

#### 

[Get-SPSecureStoreApplication](get-spsecurestoreapplication.md)
  
[Set-SPSecureStoreApplication](set-spsecurestoreapplication.md)
  
[Remove-SPSecureStoreApplication](remove-spsecurestoreapplication.md)

