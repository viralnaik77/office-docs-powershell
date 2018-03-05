---
title: "Get-SPTrustedSecurityTokenIssuer"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d64ba248-a548-45c8-8adb-87514fe72c0e

description: "Returns the trusted security token issuer object."
---

# Get-SPTrustedSecurityTokenIssuer

Returns the trusted security token issuer object.
  
```
Get-SPTrustedSecurityTokenIssuer [[-Identity] <SPTrustedSecurityTokenServicePipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Get-SPTrustedSecurityTokenService** cmdlet to return the trusted security token issuer by using the **Identity** parameter. This cmdlet returns the **SPSecurityTokenServiceManager** object. The properties on this object can be set by using the [Set-SPTrustedSecurityTokenIssuer](set-sptrustedsecuritytokenissuer.md) cmdlet and then updated back to the object. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedSecurityTokenServicePipeBind  <br/> |Specifies the ID of the trusted security token issuer object that you want to return. If you do not specify this parameter, the cmdlet returns all the objects.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedSecurityTokenServicePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-------------EXAMPLE---------- 
  
```
Get-SPTrustedSecurityTokenService
```

This example displays all trusted security token service objects from the farm.
  
## See also

#### 

[New-SPTrustedSecurityTokenIssuer](new-sptrustedsecuritytokenissuer.md)
  
[Remove-SPTrustedSecurityTokenIssuer](remove-sptrustedsecuritytokenissuer.md)
  
[Set-SPTrustedSecurityTokenIssuer](set-sptrustedsecuritytokenissuer.md)

