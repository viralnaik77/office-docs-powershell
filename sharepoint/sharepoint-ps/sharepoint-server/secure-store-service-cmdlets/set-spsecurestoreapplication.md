---
title: "Set-SPSecureStoreApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84e19022-d085-4e4e-9593-f66d6493a35e

description: "Sets properties of a Secure Store application."
---

# Set-SPSecureStoreApplication

Sets properties of a Secure Store application.
  
```
Set-SPSecureStoreApplication -Identity <SPSecureStoreApplication> [-Administrator <SPClaim[]>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-CredentialsOwnerGroup <SPClaim[]>] [-Fields <TargetApplicationField[]>] [-TargetApplication <TargetApplication>] [-TicketRedeemer <SPClaim[]>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPSecureStoreApplication** cmdlet sets properties of a Secure Store application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.SecureStoreService.PowerShellCmdlet.SPSecureStoreApplication  <br/> |Specifies the Secure Store application to update.  <br/> |
|**Administrator** <br/> |Optional  <br/> |Microsoft.SharePoint.SPClaim[]  <br/> |Specifies the administrator of the Secure Store application.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**CredentialsOwnerGroup** <br/> |Optional  <br/> |Microsoft.SharePoint.SPClaim[]  <br/> |Specifies the claims object for the groups that own the group credentials.  <br/> |
|**Fields** <br/> |Optional  <br/> |Microsoft.Office.SecureStoreService.Server.TargetApplicationField[]  <br/> |Specifies the field information for the application. The default fields are username and password.  <br/> |
|**TargetApplication** <br/> |Optional  <br/> |Microsoft.Office.SecureStoreService.Server.TargetApplication  <br/> |Specifies the target application.  <br/> |
|**TicketRedeemer** <br/> |Optional  <br/> |Microsoft.SharePoint.SPClaim[]  <br/> |Specifies the ticket redeemer claim value.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.SecureStoreService.PowerShellCmdlet.SPSecureStoreApplication  <br/> ||
|**Administrator** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim[]  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**CredentialsOwnerGroup** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim[]  <br/> ||
|**Fields** <br/> |Optional  <br/> |Microsoft.Office.SecureStoreService.Server.TargetApplicationField[]  <br/> ||
|**TargetApplication** <br/> |Optional  <br/> |Microsoft.Office.SecureStoreService.Server.TargetApplication  <br/> ||
|**TicketRedeemer** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim[]  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$targetApp.FriendlyName = "Updated Contoso Target App"
```

```
Set-SPSecureStoreApplication -Identity $application -TargetApplication $targetApp
```

This example sets a new display name  `Updated Contoso Target App` for the target application. 
  
## See also

#### 

[Get-SPSecureStoreApplication](get-spsecurestoreapplication.md)
  
[New-SPSecureStoreApplication](new-spsecurestoreapplication.md)
  
[Remove-SPSecureStoreApplication](remove-spsecurestoreapplication.md)

