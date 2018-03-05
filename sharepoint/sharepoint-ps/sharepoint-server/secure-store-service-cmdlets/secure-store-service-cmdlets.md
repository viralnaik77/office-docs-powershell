---
title: "Secure Store Service cmdlets in SharePoint Server 2016"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 2/26/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: 5e9416ff-be81-447e-8bca-66f462fb98a8
description: "Summary: Lists Windows PowerShell cmdlets that help you manage the Secure Store Service in SharePoint Server 2016."
---

# Secure Store Service cmdlets in SharePoint Server 2016

 **Summary:** Lists Windows PowerShell cmdlets that help you manage the Secure Store Service in SharePoint Server 2016. 
  
The Secure Store Service is a claims-aware authentication service that includes a secure database for storing credentials that are associated with application IDs. These application IDs can be used to authorize access to external data sources. The Secure Store Service provides the capability of securely storing credentials and associating them to specific identities or a group of identities. A common scenario for Secure Store Service is an application trying to authenticate against a system in which the current user is known by a different name or has a different account for authentication. When used with Microsoft Microsoft Business Connectivity Services, the Secure Store Service provides a means to authenticate against external data sources.
  
When you use Microsoft PowerShell cmdlets, you can create and configure a Secure Store Service instance, configure the settings of a credentials database, and configure all global settings of the Secure Store Service.
  
[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md) includes a complete list of all cmdlets in SharePoint Server 2016. 
  
|**Cmdlet name**|**Description**|
|:-----|:-----|
|[Clear-SPSecureStoreCredentialMapping](clear-spsecurestorecredentialmapping.md) <br/> |Deletes a credential mapping from a Secure Store Service application.  <br/> |
|[Clear-SPSecureStoreDefaultProvider](clear-spsecurestoredefaultprovider.md) <br/> |Clears the secure store provider.  <br/> |
|[Disable-SPSingleSignOn](disable-spsinglesignon.md) <br/> |Disables the single sign-on (SSO) service on a farm server.  <br/> |
|[Get-SPSecureStoreApplication](get-spsecurestoreapplication.md) <br/> |Returns a Secure Store application.  <br/> |
|[New-SPSecureStoreApplication](new-spsecurestoreapplication.md) <br/> |Creates a new Secure Store application.  <br/> |
|[New-SPSecureStoreApplicationField](new-spsecurestoreapplicationfield.md) <br/> |Creates a new Secure Store application fields object.  <br/> |
|[New-SPSecureStoreServiceApplication](new-spsecurestoreserviceapplication.md) <br/> |Creates a new Secure Store Service application in the farm.  <br/> |
|[New-SPSecureStoreServiceApplicationProxy](new-spsecurestoreserviceapplicationproxy.md) <br/> |Creates a new Secure Store Service application proxy in the farm.  <br/> |
|[New-SPSecureStoreTargetApplication](new-spsecurestoretargetapplication.md) <br/> |Creates a new Secure Store target application.  <br/> |
|[Remove-SPSecureStoreApplication](remove-spsecurestoreapplication.md) <br/> |Deletes a Secure Store application.  <br/> |
|[Set-SPSecureStoreApplication](set-spsecurestoreapplication.md) <br/> |Sets properties of a Secure Store application.  <br/> |
|[Set-SPSecureStoreDefaultProvider](set-spsecurestoredefaultprovider.md) <br/> |Sets or updates the secure store provider.  <br/> |
|[Set-SPSecureStoreServiceApplication](set-spsecurestoreserviceapplication.md) <br/> |Sets properties of a Secure Store Service application in the farm.  <br/> |
|[Update-SPSecureStoreApplicationServerKey](update-spsecurestoreapplicationserverkey.md) <br/> |Synchronizes the key on a server running SharePoint Server by using the Secure Store master key.  <br/> |
|[Update-SPSecureStoreCredentialMapping](update-spsecurestorecredentialmapping.md) <br/> |Sets a new credential mapping for a Secure Store Service application.  <br/> |
|[Update-SPSecureStoreGroupCredentialMapping](update-spsecurestoregroupcredentialmapping.md) <br/> |Sets a new group credential mapping for a Secure Store Service application.  <br/> |
|[Update-SPSecureStoreMasterKey](update-spsecurestoremasterkey.md) <br/> |Changes the master key of a Secure Store Service application.  <br/> |
|[Upgrade-SPSingleSignOnDatabase](upgrade-spsinglesignondatabase.md) <br/> |Migrates the application definitions from single sign-on (SSO) database to Secure Store database as target applications.  <br/> |
|[Add-SPSecureStoreSystemAccount](add-spsecurestoresystemaccount.md) <br/> |Adds an account to a designated list.  <br/> |
|[Get-SPSecureStoreSystemAccount](get-spsecurestoresystemaccount.md) <br/> |Returns a list of users from a designated list.  <br/> |
|[Remove-SPSecureStoreSystemAccount](remove-spsecurestoresystemaccount.md) <br/> |Removes a user account from a designated list.  <br/> |
   
## See also

#### 

[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md)

