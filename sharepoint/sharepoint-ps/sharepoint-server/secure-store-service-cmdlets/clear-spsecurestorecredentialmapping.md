---
title: "Clear-SPSecureStoreCredentialMapping"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e5ac1f71-b49f-4f12-8469-9c15b0ddf9fe

description: "Deletes a credential mapping from a Secure Store Service application."
---

# Clear-SPSecureStoreCredentialMapping

Deletes a credential mapping from a Secure Store Service application.
  
```
Clear-SPSecureStoreCredentialMapping -Identity <SPSecureStoreApplication> -Principal <SPClaim> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Clear-SPSecureStoreCredentialMapping** cmdlet deletes a credential mapping from a Secure Store application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**All** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the principal is deleted from all Secure Store applications.  <br/> |
|**Identity** <br/> |Required  <br/> |Microsoft.Office.SecureStoreService.PowerShellCmdlet.SPSecureStoreApplication  <br/> |Specifies the Secure Store application (that contains the principal) from which to delete the credential mapping.  <br/> |
|**Principal** <br/> |Required  <br/> |Microsoft.SharePoint.SPClaim  <br/> |Specifies the **SPClaims** object that contains the principal.  <br/> |
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context for which the credential mapping will be deleted.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**All** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Identity** <br/> |Required  <br/> |Microsoft.Office.SecureStoreService.PowerShellCmdlet.SPSecureStoreApplication  <br/> ||
|**Principal** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim  <br/> ||
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$ssApp = Get-SPSecureStoreApplication -ServiceContext http://contoso -Name "ContosoTargetApplication"
```

```
$userClaim = New-SPClaimsPrincipal -Identity "CONTOSO\janedoe" -IdentityType WindowsSamAccountName
```

```
Clear-SPSecureStoreCredentialMapping -Identity $ssApp -Principal $userClaim
```

This example deletes the credential mapping from the target application  `ContosoTargetApplication` for the user with alias  `johndoe` and domain  `CONTOSO`.
  
## See also

#### 

[Update-SPSecureStoreCredentialMapping](update-spsecurestorecredentialmapping.md)

