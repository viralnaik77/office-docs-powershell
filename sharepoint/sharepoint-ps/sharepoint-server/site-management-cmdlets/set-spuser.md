---
title: "Set-SPUser"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a412b5e1-b330-4992-a10d-7593078684a7

description: "Configures properties of an existing user."
---

# Set-SPUser

Configures properties of an existing user.
  
```
Set-SPUser [-Identity] <SPUserPipeBind> [-AddPermissionLevel <String[]>] [-AssignmentCollection <SPAssignmentCollection>] [-ClearPermissions <SwitchParameter>] [-Confirm [<SwitchParameter>]] [-DisplayName <String>] [-Email <String>] [-Group <SPGroupPipeBind>] [-IsSiteCollectionAdmin <SwitchParameter>] [-PassThru <SwitchParameter>] [-RemovePermissionLevel <String[]>] [-SyncFromAD <SwitchParameter>] [-Web <SPWebPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPUser** cmdlet configures properties of an existing user. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserPipeBind  <br/> |Specifies the login name, or **SPUser** object of the user to be returned.  <br/> The type must be the login name of an existing user in the form, domain\user.  <br/> |
|**AddPermissionLevel** <br/> |Optional  <br/> |System.String[]  <br/> |Specifies the permission level to add to the user.  <br/> The value must be one of the following options:  <br/> **Contribute** - Can view, add, update, and delete list items and documents.  <br/> **Design** - Can view, add, update, delete, approve, and customize documents  <br/> **Full Control** - Has full control for all documents  <br/> **Limited Access** - Can view specific lists, document libraries, list items, folders, or documents when permissions are granted.  <br/> **Read** - Can view pages and list items and download documents  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**ClearPermissions** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Deletes all assigned permissions from the user. If Clear and Add values exist, permissions are first cleared, and then new permissions are added.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DisplayName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the new display name of the user.  <br/> The type must be a valid name.  <br/> |
|**Email** <br/> |Optional  <br/> |System.String  <br/> |Specifies the new email address of the user.  <br/> |
|**Group** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPGroupPipeBind  <br/> |Adds the user to an existing group in the given site.  <br/> |
|**IsSiteCollectionAdmin** <br/> |Optional  <br/> |none  <br/> |Specifies whether to set the user as a site collection administrator.  <br/> |
|**PassThru** <br/> |Optional  <br/> |none  <br/> |If not provided, indicates that this cmdlet has no output. If provided, this parameter indicates that the **SPUser** object for this user is to be returned.  <br/> |
|**RemovePermissionLevel** <br/> |Optional  <br/> |System.String[]  <br/> |Removes the permission level from the user.  <br/> |
|**SyncFromAD** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |If provided, specifies that user information will be synchronized from the user directory store.  <br/> |
|**Web** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the name of the URL or GUID to be used as a scope. This parameter is not needed if the **SPUser** object is provided as the identity.  <br/> The value must be an authentic URL, in the form http://server_name, or GUID, in the form 1234-5678-9807.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserPipeBind  <br/> ||
|**AddPermissionLevel** <br/> |Optional  <br/> |System.String[]  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**ClearPermissions** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DisplayName** <br/> |Optional  <br/> |System.String  <br/> ||
|**Email** <br/> |Optional  <br/> |System.String  <br/> ||
|**Group** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPGroupPipeBind  <br/> ||
|**IsSiteCollectionAdmin** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**PassThru** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**RemovePermissionLevel** <br/> |Optional  <br/> |System.String[]  <br/> ||
|**SyncFromAD** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Web** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
Set-SPUser -Identity 'Contoso\jdow' -Web http://test -AddPermissionLevel "Contributor"
```

This example sets a user ( `Contoso\jdow`) to be a contributor on  `http://test`.
  
## See also

#### 

[Get-SPUser](get-spuser.md)
  
[New-SPUser](new-spuser.md)
  
[Remove-SPUser](remove-spuser.md)
  
[Move-SPUser](move-spuser.md)

