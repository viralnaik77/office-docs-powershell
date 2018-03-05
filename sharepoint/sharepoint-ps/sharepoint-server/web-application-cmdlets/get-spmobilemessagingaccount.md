---
title: "Get-SPMobileMessagingAccount"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 03b69f50-07ec-4feb-bc9c-567237d200ea

description: "Retrieves mobile messaging accounts for the specified Web application."
---

# Get-SPMobileMessagingAccount

Retrieves mobile messaging accounts for the specified Web application.
  
```
Get-SPMobileMessagingAccount [[-Identity] <SPMobileMessagingAccountPipeBind>] -WebApplication <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPMobileMessagingAccount** cmdlet retrieves the specified mobile messaging accounts for the specified Web application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPMobileMessagingAccountPipeBind  <br/> |Specifies whether to return either Short Message Service (SMS) or Multimedia Messaging Service (MMS) account information. Valid values are: **SMS** and **MMS**. If you do not specify this parameter, account information is returned for both SMS and MMS.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the identity of the Web application to delete. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid Web application name (for example, WebApplication1212); or a valid name (for example, WebApp2423).  <br/> You either must specify **WebApplication** or must use the **HostHeader** switch and specify the full URL in the **Identity** parameter.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPMobileMessagingAccountPipeBind  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Get-SPMobileMessagingAccount -WebApplication http://sitename
```

This example retrieves the current mobile account settings information of the Web application  `http://sitename`.
  
## See also

#### 

[Set-SPMobileMessagingAccount](set-spmobilemessagingaccount.md)

