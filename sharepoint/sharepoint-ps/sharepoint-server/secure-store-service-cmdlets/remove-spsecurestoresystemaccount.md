---
title: "Remove-SPSecureStoreSystemAccount"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: af5e1eae-5a7d-485e-862d-cf784cb004a1

description: "Removes a user account from a designated list."
---

# Remove-SPSecureStoreSystemAccount

Removes a user account from a designated list.
  
```
Remove-SPSecureStoreSystemAccount [-Identity] <SPSecureStoreSystemAccountPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Remove-SPSecureStoreSystemAccount** cmdlet to remove a user account from a designated list of accounts which will be considered a system account. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.SecureStoreService.PowerShellCmdlet.SPSecureStoreSystemAccountPipeBind  <br/> |Specifies the name, object, or GUID to remove.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.SecureStoreService.PowerShellCmdlet.SPSecureStoreSystemAccountPipeBind  <br/> ||
|AssignmentCollection  <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------EXAMPLE 1----------
  
```
Remove-SPSecureStoreSystemAccount -Identity contoso\jdoe
```

This example removes a specific user name jdoe by using the **Identity** parameter. 
  
--------------EXAMPLE 2----------
  
```
Get-SPSecureStoreSystemAccount | Where-Object -filter {$_.AccountName -eq 'Contoso\admin'} | Remove-SPSecureStoreSystemAccount
```

This example removes the admin, user from the contoso domain by filtering the results from the **Get-SPSecureStoreSystemAccount** cmdlet. 
  
## See also

#### 

[Add-SPSecureStoreSystemAccount](add-spsecurestoresystemaccount.md)
  
[Get-SPSecureStoreSystemAccount](get-spsecurestoresystemaccount.md)

