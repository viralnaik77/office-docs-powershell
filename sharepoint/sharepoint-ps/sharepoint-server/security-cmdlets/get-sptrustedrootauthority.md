---
title: "Get-SPTrustedRootAuthority"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3a6cfdd7-0b7f-4464-a057-6c0ac590b218

description: "Returns a trusted root authority."
---

# Get-SPTrustedRootAuthority

Returns a trusted root authority.
  
```
Get-SPTrustedRootAuthority [[-Identity] <SPTrustedRootAuthorityPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPTrustedRootAuthority** cmdlet returns a trusted root authority. If a certificate file is used, it must have only one X509 certificate without private keys, otherwise an exception is raised. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedRootAuthorityPipeBind  <br/> |Specifies the trusted root authority to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a trusted root authority (for example, WFEFarm1); or an instance of a valid **SPTrustedRootAuthority** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedRootAuthorityPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$rootauthority=Get-SPTrustedRootAuthority -Identity "WFEFarm1"
```

This example creates a new trusted root authority,  `WFEFarm1`.
  
## See also

#### 

[New-SPTrustedRootAuthority](new-sptrustedrootauthority.md)
  
[Set-SPTrustedRootAuthority](set-sptrustedrootauthority.md)
  
[Remove-SPTrustedRootAuthority](remove-sptrustedrootauthority.md)

