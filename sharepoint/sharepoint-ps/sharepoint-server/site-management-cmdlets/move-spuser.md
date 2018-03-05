---
title: "Move-SPUser"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 9/14/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 783cad23-5442-46b2-af98-79e0b8e4977d

description: "Migrates a user account in SharePoint 2013 Products."
---

# Move-SPUser

Migrates a user account in SharePoint 2013 Products.
  
```
Move-SPUser [-Identity] <SPUserPipeBind> -NewAlias <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-IgnoreSID <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Move-SPUser** cmdlet migrates user access from one domain user account to another. If an entry for the new login name already exists, the entry is marked for deletion to make way for the migration. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserPipeBind  <br/> |The type must be a valid login name or GUID of the user, in the form DOMAIN\username or 1234-5678-9876-0987 or CLAIMPREFIX|DOMAIN\username.  <br/> > [!NOTE]> If the claim prefix is not used, then the migrated user with domain\username won't be able to login until we migrate him to the claim prefix.           |
|**NewAlias** <br/> |Required  <br/> |System.String  <br/> |Specifies the new login name of the user account.  <br/> The type must be a valid login name, in the form DOMAIN\username or CLAIMPREFIX|DOMAIN\username.  <br/> > [!NOTE]> If the claim prefix is not used, then the migrated user with domain\username won't be able to login until we migrate him to the claim prefix.           |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**IgnoreSID** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Indicates (if present) that Active Directory will not be queried for the SID history attribute to ensure that the new login name is correspondent to the old login name.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserPipeBind  <br/> ||
|**NewAlias** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**IgnoreSID** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1------------------
  
```
Move-SPUser -Identity "DOMAIN\JaneDoe" -NewAlias "Domain\JaneSmith"
```

This example migrates  `DOMAIN\JaneDoe` to the new account of  `DOMAIN\JaneSmith`.
  
------------------EXAMPLE 2------------------
  
```
Move-SPUser -Identity "DomainA\JaneDoe" -NewAlias "DomainB\JaneDoe"
```

This example migrates  `DOMAIN\JaneDoe` from DomainA to the new account of  `DOMAINB\JaneDoe` in DomainB. 
  
------------------EXAMPLE 3------------------
  
```
Move-SPUser -Identity "i:0#.w|Domain\JaneDoe" -NewAlias "i:05.t|adfs|Domain\JaneDoe"
```

This example migrates the acount i:0#.w|Domain\JaneDoe from Windows authentication to the new account of i:05.t|adfs|Domain\JaneDoe in SAML authentication.
  
------------------EXAMPLE 4------------------
  
```
Move-SPUser -Identity "i:0#.w|DomainA\JaneDoe" -NewAlias "i:0#.f|mymembershipprovider|DomainB\JaneDoe"
```

This example migrates the acount i:0#.w|DomainA\JaneDoe from DomainA with Windows authentication to the new account of i:0#.f|mymembershipprovider|DomainB\JaneDoe in DomainB with Forms-based authentication.
  
## See also

#### 

[New-SPUser](new-spuser.md)
  
[Set-SPUser](set-spuser.md)
  
[Remove-SPUser](remove-spuser.md)
  
[Get-SPUser](get-spuser.md)

