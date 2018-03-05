---
title: "Remove-SPUser"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cc60e125-781c-45bb-8e91-896fe8a230c1

description: "Removes a user from a Web site."
---

# Remove-SPUser

Removes a user from a Web site.
  
```
Remove-SPUser [-Identity] <SPUserPipeBind> -Web <SPWebPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Group <SPGroupPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPUser** cmdlet specifies the identity and user group from which a user is to be removed. The **Remove-SPUser** cmdlet does not remove the user from Active Directory Domain Services (AD DS). 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserPipeBind  <br/> |Specifies the GUID, the user name, or **SPUser** object to remove.  <br/> The type must be a valid GUID of the user, in the form 1234-5678-9876-0987.  <br/> |
|**Web** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the name of the URL or GUID from which the user is to be removed. This parameter is needed only if the identity provided is the user name.  <br/> The type must be a valid URL, in the form http://server_name, or a GUID, in the form 1234-5678-9807.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Group** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPGroupPipeBind  <br/> |The user only gets removed from that group. Otherwise, the user gets removed from the site.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserPipeBind  <br/> ||
|**Web** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Group** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPGroupPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1-----------------------
  
```
Remove-SPUser "Contoso \jdoe" -web http://test/web1
```

```
Get-SPWeb "http://test/web1" | Remove-SPUser "Contoso\jdoe"
```

This example removes the user ( `Contoso\jdoe`) from the Web application  `http://test/web1`.
  
------------------EXAMPLE 2-----------------------
  
```
Get-SPSite http://contoso.com |Get-SPWeb |Remove-SPUser "Contoso\jdoe"
```

This syntax removes the user ( `Contoso\Jdoe`) from every Web in a site collection located at  `http://contoso.com`.
  
## See also

#### 

[Get-SPUser](get-spuser.md)
  
[Set-SPUser](set-spuser.md)
  
[New-SPUser](new-spuser.md)
  
[Remove-SPUser](remove-spuser.md)

