---
title: "Remove-SPSite"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f2c49315-8eed-49ec-8a32-dc15a008d0dc

description: "Completely deletes an existing site collection and all subsites."
---

# Remove-SPSite

Completely deletes an existing site collection and all subsites.
  
```
Remove-SPSite [-Identity] <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DeleteADAccounts <SwitchParameter>] [-GradualDelete <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPSite** cmdlet completely deletes an existing site collection and all subsites. This operation cannot be undone. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the identity of the site to delete. The identity can be either a valid URL, in the form http://server_name; a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an **SPSite** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DeleteADAccounts** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forces deletion of user accounts from Active Directory Domain Services (AD DS). This applies when in AD DS account creation mode and the value of this parameter is **True**, AD DS accounts associated with the site collection are also deleted from AD DS.  <br/> |
|**GradualDelete** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |If provided, occurs gradually to use less system load. This operation is strongly recommended for deleting very large sites.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

------------------EXAMPLE-----------------------
  
```
Remove-SPSite -Identity "http://sitename" -GradualDelete -Confirm:$False
```

This example removes the given site collection and all included sites by using  `GradualDelete`; confirmation has been suppressed.
  
## See also

#### 

[Get-SPSite](get-spsite.md)
  
[Set-SPSite](set-spsite.md)
  
[New-SPSite](new-spsite.md)
  
[Backup-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/backup-and-recovery-cmdlets/backup-spsite.md)
  
[Remove-SPSite](remove-spsite.md)
  
[Move-SPSite](move-spsite.md)
  
[Restore-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/backup-and-recovery-cmdlets/restore-spsite.md)

