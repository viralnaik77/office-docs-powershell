---
title: "Remove-SPManagedAccount"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6212010e-b873-47d7-9665-d4b9e94f28b4

description: "Removes a managed account registration from the farm."
---

# Remove-SPManagedAccount

Removes a managed account registration from the farm.
  
```
Remove-SPManagedAccount [-Identity] <SPManagedAccountPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Remove-SPManagedAccount** cmdlet removes account registration from the configuration database within the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPManagedAccountPipeBind  <br/> |Specifies the full name or partial name of the managed accounts to retrieve.  <br/> The type must be a valid account name, in the form Domain\User, or a GUID, in the form 1234-3456-09876.  <br/> |
|**NewPassword** <br/> |Required  <br/> |System.Security.SecureString  <br/> |Specifies a secure string for the new password (that is, $MySecureString).Works in conjunction with the **ChangePassword** parameter.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**ChangePassword** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether a password is to be changed. Works in conjunction with the **NewPassword** parameter. When the ChangePassword value is set, a secure string value is required for the **NewPassword** parameter (that is, $MySecureString).  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPManagedAccountPipeBind  <br/> ||
|**NewPassword** <br/> |Required  <br/> |System.Security.SecureString  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**ChangePassword** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

----------------------EXAMPLE-------------------
  
```
Remove-SPManagedAccount -Identity DOMAIN\ServiceAcct
```

This example removes the DOMAIN\ServiceAcct managed account from the farm.
  
## See also

#### 

[Get-SPManagedAccount](get-spmanagedaccount.md)
  
[New-SPManagedAccount](new-spmanagedaccount.md)
  
[Set-SPManagedAccount](set-spmanagedaccount.md)

