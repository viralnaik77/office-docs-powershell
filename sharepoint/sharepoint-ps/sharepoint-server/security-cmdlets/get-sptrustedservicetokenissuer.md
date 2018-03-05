---
title: "Get-SPTrustedServiceTokenIssuer"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc6e4563-59ae-4c0f-8d2c-cdc09e313534

description: "Returns the object that represents the farm trust."
---

# Get-SPTrustedServiceTokenIssuer

Returns the object that represents the farm trust.
  
```
Get-SPTrustedServiceTokenIssuer [[-Identity] <SPTrustedServiceTokenIssuerPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPTrustedServiceTokenIssuer** cmdlet returns the object that represents the farm trust. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedServiceTokenIssuerPipeBind  <br/> |Specifies the trusted service token issuer to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a trusted service token issuer (for example, WFEFarm1); or an instance of a valid **SPTrustedRootAuthority** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedServiceTokenIssuerPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Get-SPTrustedServiceTokenIssuer "WFEFarm1"
```

This example gets the trusted services token issuer  `WFEFarm1`.
  
## See also

#### 

[Set-SPTrustedServiceTokenIssuer](set-sptrustedservicetokenissuer.md)
  
[New-SPTrustedServiceTokenIssuer](new-sptrustedservicetokenissuer.md)
  
[Remove-SPTrustedServiceTokenIssuer](remove-sptrustedservicetokenissuer.md)

