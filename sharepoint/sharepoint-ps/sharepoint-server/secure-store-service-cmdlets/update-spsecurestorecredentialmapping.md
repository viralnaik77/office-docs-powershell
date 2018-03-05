---
title: "Update-SPSecureStoreCredentialMapping"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2b36a396-c89a-4366-ac91-b962e7d4d058

description: "Sets a new credential mapping for a Secure Store Service application."
---

# Update-SPSecureStoreCredentialMapping

Sets a new credential mapping for a Secure Store Service application.
  
```
Update-SPSecureStoreCredentialMapping -Identity <SPSecureStoreApplication> -Principal <SPClaim> -Values <SecureString[]> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Update-SPSecureStoreCredentialMapping** cmdlet sets a new credential mapping for a Secure Store Service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.SecureStoreService.PowerShellCmdlet.SPSecureStoreApplication  <br/> |Specifies the Secure Store Service application (that contains the principal) from which to delete the credential mapping.  <br/> |
|**Principal** <br/> |Required  <br/> |Microsoft.SharePoint.SPClaim  <br/> |Specifies the SPClaims object that contains the principal.  <br/> |
|**Values** <br/> |Required  <br/> |System.Security.SecureString[]  <br/> |Specifies the field values for the credential mapping.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.SecureStoreService.PowerShellCmdlet.SPSecureStoreApplication  <br/> ||
|**Principal** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim  <br/> ||
|**Values** <br/> |Required  <br/> |System.Security.SecureString[]  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$ssApp = Get-SPSecureStoreApplication -ServiceContext http://contoso -Name "ContosoTargetApplication"
$firstCredential = ConvertTo-SecureString "LOBDATABASE\jdoe" -AsPlainText -Force
$secondCredential = ConvertTo-SecureString "abcDEF123$%^" -AsPlainText -Force
$credentialValues = $firstCredential,$secondCredential
$userClaim = New-SPClaimsPrincipal -Identity "CONTOSO\janedoe" -IdentityType WindowsSamAccountName
Update-SPSecureStoreCredentialMapping -Identity $ssApp -Values $credentialValues -Principal $userClaim
```

This example updates a credential mapping for the given site and the target application  `ContosoTargetApplication`, for the user with the identity  `janedoe` on domain  `CONTOSO`. This user is mapped to a pair of credential values on the External System with a username of identity  `jdoe` on domain  `LOBDATABASE` and password  `abcDEF123$%^`.
  
## See also

#### 

[Clear-SPSecureStoreCredentialMapping](clear-spsecurestorecredentialmapping.md)
  
[Update-SPSecureStoreGroupCredentialMapping](update-spsecurestoregroupcredentialmapping.md)

