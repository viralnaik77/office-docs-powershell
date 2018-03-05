---
title: "Revoke-SPObjectSecurity"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4e7583ab-5b8d-47c2-a9eb-2cf525ae07d8

description: "Removes a security principal from a SPObjectSecurity object."
---

# Revoke-SPObjectSecurity

Removes a security principal from a **SPObjectSecurity** object. 
  
```
Revoke-SPObjectSecurity [-Identity] <SPObjectSecurity> [-Principal] <SPClaim> [[-Rights] <String[]>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Revoke-SPObjectSecurity** cmdlet to remove a security principal, such as a user, from a **SPObjectSecurity** object. An **SPObjectSecurity** object is a common object that is used to represent the security access control list (ACL) of SharePoint administrative objects, in particular service applications. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.AccessControl.SPObjectSecurity  <br/> |Specifies the **SPObjectSecurity** object from which the security principal is removed. You can use the Get- **SPServiceApplicationSecurity** cmdlet to get a **SPObjectSecurity** object .  <br/> |
|**Principal** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim  <br/> |Specifies the principal for whom the rights are removed.  <br/> The type must a valid name a principal; for example, Full Control.  <br/> |
|**Rights** <br/> |Optional  <br/> |System.String[]  <br/> |Specifies the rights of the principal to revoke.  <br/> The type must a valid array of strings that represents the rights of the principal to revoke.  <br/> |
|**All** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that all security principals are removed from the specified **SPObjectSecurity** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.AccessControl.SPObjectSecurity  <br/> ||
|**Principal** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim  <br/> ||
|**Rights** <br/> |Optional  <br/> |System.String[]  <br/> ||
|**All** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$security = Get-SPServiceApplicationSecurity $serviceApp -AdminRevoke-SPObjectSecurity $security "domain\user"Set-SPServiceApplicationSecurity $serviceApp -Admin $security
```

This example retrieves the **SPObjectSecurity** object corresponding to the administrator ACL on a service application, and removes a user from that ACL. The removed an administrator for the service application  `$serviceApp`.
  
## See also

#### 

[Grant-SPObjectSecurity](grant-spobjectsecurity.md)
  
[Get-SPServiceApplicationSecurity](get-spserviceapplicationsecurity.md)

