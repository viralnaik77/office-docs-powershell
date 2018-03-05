---
title: "New-SPUser"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b8d7f8df-d5df-4497-a55b-dbe56b1c6fbb

description: "Adds an existing user to a SharePoint site with the designated permissions."
---

# New-SPUser

Adds an existing user to a SharePoint site with the designated permissions.
  
```
New-SPUser [-UserAlias] <String> -Web <SPWebPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DisplayName <String>] [-Email <String>] [-Group <SPGroupPipeBind>] [-PermissionLevel <String[]>] [-SiteCollectionAdmin <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **New-SPUser** cmdlet adds an existing user to a SharePoint web site with the designated permissions. This user has the given permissions in all subsites that inherit permissions. The user account must already exist in the user directory. 
  
If your environment is in Active Directory mode, the user must already exist in Active Directory Domain Services (AD DS) and only the **UserAlias** parameter is required; all other fields are pulled from AD DS. If only an alias is given and the farm is in Active Directory Account Create mode, the **Email** parameter is also required. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**UserAlias** <br/> |Required  <br/> |System.String  <br/> |Specifies the user alias from Active Directory Domain Services (AD DS).  <br/> |
|**Web** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the URL or GUID of the web on which to create this user.  <br/> The type must be a valid URL, in the form http://server_name, or a GUID, in the form 1234-5678-9876-0987.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DisplayName** <br/> |Optional  <br/> |System.String  <br/> |Specifies a string that contains the display name of the user.  <br/> The type must be a valid user name; for example, Joe.  <br/> |
|**Email** <br/> |Optional  <br/> |System.String  <br/> |Specifies the email address of the new user.  <br/> The type must be a valid email address, in the form someone@contoso.com.  <br/> |
|**Group** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPGroupPipeBind  <br/> |Specifies the user group to which the new user belongs.  <br/> |
|**PermissionLevel** <br/> |Optional  <br/> |System.String[]  <br/> |Adds a user to a permission level.  <br/> The type must be a valid permission level for the web application; for example, **Full Control**, **Read**, **Contribute**, or **All**.  <br/> |
|**SiteCollectionAdmin** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether to add the user as an administrator to the site collection.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**UserAlias** <br/> |Required  <br/> |System.String  <br/> ||
|**Web** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DisplayName** <br/> |Optional  <br/> |System.String  <br/> ||
|**Email** <br/> |Optional  <br/> |System.String  <br/> ||
|**Group** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPGroupPipeBind  <br/> ||
|**PermissionLevel** <br/> |Optional  <br/> |System.String[]  <br/> ||
|**SiteCollectionAdmin** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1----------------------
  
```
New-SPUser -UserAlias 'Contoso\Jdow' -DisplayName 'Jane Dow' -Web 'http://contoso.com'
```

This example adds a new user named  `Jane Dow` to the  `Contoso` domain. 
  
------------------EXAMPLE 2----------------------
  
```
Get-SPWeb 'http://sitename' | New-SPUser -UserAlias 'Contoso\Jdow'
```

This example adds  `Contoso\Jdow` to all webs in the  `http://sitename` site collection. Because this site collection uses inherited permissions, only the top-level web site needs to be touched. 
  
## See also

#### 

[Get-SPUser](get-spuser.md)
  
[Set-SPUser](set-spuser.md)
  
[Move-SPUser](move-spuser.md)
  
[Remove-SPUser](remove-spuser.md)

