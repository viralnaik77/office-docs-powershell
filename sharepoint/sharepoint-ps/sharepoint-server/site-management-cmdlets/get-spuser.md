---
title: "Get-SPUser"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 9/8/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1ec026e1-2480-4c31-bc23-3d0692d51ef9

description: "Returns the user account or accounts that match a given search criteria."
---

# Get-SPUser

Returns the user account or accounts that match a given search criteria.
  
```
Get-SPUser [[-Identity] <SPUserPipeBind>] -Web <SPWebPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Group <SPGroupPipeBind>] [-Limit <String>]
```

## Detailed Description

The **Get-SPUser** cmdlet returns all SharePoint user accounts that match the scope given by the **Identity**, **Web**, or **Group** parameters. 
  
The **Identity** parameter can use the alias of a user for returning exact matches. However, a scope must be provided if the **Get-SPUser** cmdlet is to work. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUserPipeBind  <br/> |Specifies the login name of the user to be returned.  <br/> The Identity must be a valid user name, in the form of "Domain\user" for a Windows Classic user or "i:0#.w\Domain\user" (or user name with the appropriate claims format) for a claims user or an integer corresponding to the user id in the SharePoint user info list.  <br/> |
|**Web** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the Web site to be used as a scope.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh of a valid name of a SharePoint Foundation 2013 Web site (for example, MySPSite1); or an instance of a valid **SPWeb** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Group** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPGroupPipeBind  <br/> |Specifies the user group to which the new user belongs.  <br/> |
|**Limit** <br/> |Optional  <br/> |System.String  <br/> |Specifies the maximum number of users to return. The default value is **500**. To get all of the possible items, enter 'All'.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUserPipeBind  <br/> ||
|**Web** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Group** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPGroupPipeBind  <br/> ||
|**Limit** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Get-SPUser -Web "http://zsharepoint2" -Group "Viewers"
```

This example returns all members of the group  `Viewers` on the Web site  `http://zsharepoint2`.
  
## See also

#### 

[Move-SPUser](move-spuser.md)
  
[New-SPUser](new-spuser.md)
  
[Set-SPUser](set-spuser.md)
  
[Remove-SPUser](remove-spuser.md)

