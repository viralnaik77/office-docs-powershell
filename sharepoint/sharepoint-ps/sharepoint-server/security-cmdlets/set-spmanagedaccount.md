---
title: "Set-SPManagedAccount"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 320204fe-f72f-40c6-9b1f-e7a3ddb0aca3

description: "Configures the managed account."
---

# Set-SPManagedAccount

Configures the managed account.
  
```
Set-SPManagedAccount [-Identity] <SPManagedAccountPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-EmailNotification <Int32>] [-PreExpireDays <Int32>] [-Schedule <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Set-SPManagedAccount** cmdlet sets the properties on the given managed account. 
  
You can use this cmdlet to change the password expiration and notification settings for the managed account: Use the default parameter set. Additionally, you can use this cmdlet to change the password for the managed account to automatically generated passwords on a set schedule: Use the parameter set that includes the **AutoGeneratePassword** parameter. You can also use this cmdlet to change the password for the managed account to a new value, known to the administrator: Use the parameter set that includes the **SetNewPassword** parameter. Finally, you can use this cmdlet to change the password for the managed account to an existing value that has been already been changed in Active Directory Domain Services (AD DS): Use the parameter set that includes the **UseExistingPassword** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPManagedAccountPipeBind  <br/> |Specifies the full name or partial name of the managed accounts to retrieve.  <br/> The type must be a valid account name, in the form Domain\User, or a GUID, in the form 1234-3456-09876.  <br/> |
|**ConfirmPassword** <br/> |Required  <br/> |System.Security.SecureString  <br/> |Confirms the new password for this managed account.  <br/> |
|**ExistingPassword** <br/> |Required  <br/> |System.Security.SecureString  <br/> |Sets the password for this managed account to an existing value that has already been changed in Active Directory Domain Services (AD DS).  <br/> |
|**NewPassword** <br/> |Required  <br/> |System.Security.SecureString  <br/> |Sets a new password for the managed account  <br/> |
|**Password** <br/> |Required  <br/> |System.Security.SecureString  <br/> |Sets a password for the managed account.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**AutoGeneratePassword** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Automatically generates a new password.  <br/> The type must be either of the following values:  <br/> - **True** <br/> - **False** <br/> The default value is **False**.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**EmailNotification** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of days before password change to begin e-mail notifications.  <br/> The default value is **5**.  <br/> |
|**PreExpireDays** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of days before expiration to schedule password change.  <br/> The default value is **2**.  <br/> |
|**Schedule** <br/> |Optional  <br/> |System.String  <br/> |Specifies the new schedule on which the password change job is to run.  <br/> |
|**SetNewPassword** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Sets the password to the new value that is passed in, and changes the value in AD DS.  <br/> The type must be either of the following values:  <br/> - **True** <br/> - **False** <br/> The default value is **False**.  <br/> |
|**UseExistingPassword** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Sets the password to a new value passed in where the value is already changed in AD DS.  <br/> The type must be either of the following values:  <br/> - **True** <br/> - **False** <br/> The default value is **False**.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPManagedAccountPipeBind  <br/> ||
|**ConfirmPassword** <br/> |Required  <br/> |System.Security.SecureString  <br/> ||
|**ExistingPassword** <br/> |Required  <br/> |System.Security.SecureString  <br/> ||
|**NewPassword** <br/> |Required  <br/> |System.Security.SecureString  <br/> ||
|**Password** <br/> |Required  <br/> |System.Security.SecureString  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**AutoGeneratePassword** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**EmailNotification** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**PreExpireDays** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**Schedule** <br/> |Optional  <br/> |System.String  <br/> ||
|**SetNewPassword** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**UseExistingPassword** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
$m = Get-SPManagedAccount -Identity "DOMAINx\UserY"
```

```
Set-SPManagedAccount -Identity $m -AutoGeneratePassword true
```

This example displays an explicit managed account if it exists, and then attempts to update it to use automatically generated passwords.
  
## See also

#### 

[Get-SPManagedAccount](get-spmanagedaccount.md)
  
[New-SPManagedAccount](new-spmanagedaccount.md)
  
[Remove-SPManagedAccount](remove-spmanagedaccount.md)

