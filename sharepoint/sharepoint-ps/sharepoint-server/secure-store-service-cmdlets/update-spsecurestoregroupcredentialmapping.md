---
title: "Update-SPSecureStoreGroupCredentialMapping"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: efa2b0d6-bad9-422d-acad-1f8ac60db5f5

description: "Sets a new group credential mapping for a Secure Store Service application."
---

# Update-SPSecureStoreGroupCredentialMapping

Sets a new group credential mapping for a Secure Store Service application.
  
```
Update-SPSecureStoreGroupCredentialMapping -Identity <SPSecureStoreApplication> -Values <SecureString[]> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Update-SPSecureStoreGroupCredentialMapping** cmdlet sets a new group credential mapping for a Secure Store Service application. Group credentials are a set of credentials that are associated with multiple identities. Target applications will get credentials for a Secure Store application by using the current user. If the current user meets the authorization rule defined in the Secure Store application for the group credentials, then the data is provided. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.SecureStoreService.PowerShellCmdlet.SPSecureStoreApplication  <br/> |Specifies the Secure Store application (that contains the principal) from which to delete the credential mapping.  <br/> |
|**Values** <br/> |Required  <br/> |System.Security.SecureString[]  <br/> |Specifies the field values for the credential mapping.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.SecureStoreService.PowerShellCmdlet.SPSecureStoreApplication  <br/> ||
|**Values** <br/> |Required  <br/> |System.Security.SecureString[]  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$ssApp = Get-SPSecureStoreApplication -ServiceContext http://contoso -Name "ContosoGroupTargetApplication"
$firstCredential = ConvertTo-SecureString "LOBDATABASE\fulltimeemployees" -AsPlainText -Force
$secondCredential = ConvertTo-SecureString "abcDEF123$%^" -AsPlainText -Force
$credentialValues = $firstCredential,$secondCredential
Update-SPSecureStoreGroupCredentialMapping -Identity $ssApp -Values $credentialValues
```

This example adds a credential mapping for the target application  `ContosoGroupTargetApplication`, for all users in this group target application. These users are mapped to a pair of credential values on the External System with a username of identity  `fulltimeemployees` on domain  `LOBDATABASE` and with password  `abcDEF123$%^`.
  
## See also

#### 

[Update-SPSecureStoreCredentialMapping](update-spsecurestorecredentialmapping.md)
  
[Clear-SPSecureStoreCredentialMapping](clear-spsecurestorecredentialmapping.md)

