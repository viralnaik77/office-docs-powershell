---
title: "Grant-SPObjectSecurity"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 496caa92-2ff4-4048-ab7d-57d8c835bf2b
description: "Adds a new security principal to an SPObjectSecurity object."
---

# Grant-SPObjectSecurity

Adds a new security principal to an **SPObjectSecurity** object. 
  
```
Grant-SPObjectSecurity [-Identity] <SPObjectSecurity> [-Principal] <SPClaim> [-Rights] <String[]> [-AssignmentCollection <SPAssignmentCollection>] [-Replace <SwitchParameter>]
```

## Detailed Description

The **Grant-SPObjectSecurity** cmdlet adds a new security principal, such as a user, to a **SPObjectSecurity** object. An **SPObjectSecurity** object is a common object that is used to represent the security access control list (ACL) of SharePoint administrative objects, in particular, service applications. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.AccessControl.SPObjectSecurity  <br/> |Specifies the **SPObjectSecurity** object to which the new security principal is added. You can use the **Get-SPServiceApplicationSecurity** cmdlet to get a **SPObjectSecurity** object .  <br/> |
|**Principal** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim  <br/> |Specifies the principal to whom the rights apply.  <br/> The type must a valid name a principal; for example, Full Control.  <br/> |
|**Rights** <br/> |Required  <br/> |System.String[]  <br/> |Specifies the rights granted to the principal.  <br/> The type must a valid array of strings that represents the rights granted to the principal.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.  <br/> |
|**Replace** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Replaces the existing rights on the **SPObjectSecurity** object with the new rights specified. If this parameter is not specified, the new rights are added to the existing rights.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.AccessControl.SPObjectSecurity  <br/> ||
|**Principal** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim  <br/> ||
|**Rights** <br/> |Required  <br/> |System.String[]  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Replace** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$security = Get-SPServiceApplicationSecurity $serviceApp -AdminGrant-SPObjectSecurity $security $principal "Full Control"Set-SPServiceApplicationSecurity $serviceApp -Admin $security
```

This example retrieves the **SPObjectSecurity** object corresponding to the administrator ACL on a service application, and adds a new user principal to that ACL. The new user is an administrator for the service application  `$serviceApp`.
  
## See also

#### 

[Revoke-SPObjectSecurity](revoke-spobjectsecurity.md)
  
[Get-SPServiceApplicationSecurity](get-spserviceapplicationsecurity.md)

