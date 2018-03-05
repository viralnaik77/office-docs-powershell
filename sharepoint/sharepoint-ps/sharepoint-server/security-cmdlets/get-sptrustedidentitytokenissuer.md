---
title: "Get-SPTrustedIdentityTokenIssuer"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a690ca77-b4b5-4cd1-842a-3ea3ca13ea84

description: "Returns an identity provider."
---

# Get-SPTrustedIdentityTokenIssuer

Returns an identity provider.
  
```
Get-SPTrustedIdentityTokenIssuer [[-Identity] <SPTrustedIdentityTokenIssuerPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPTrustedIdentityTokenIssuer** cmdlet returns an identity provider. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIdentityProviderPipeBind  <br/> |Specifies the identity provider to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of identity provider (for example, LiveID STS); or an instance of a valid **SPIdentityProvider** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------------------EXAMPLE 1------------------------
  
```
$trustedsts=Get-SPTrustedIdentityTokenIssuer "LiveIDSTS"
```

This example gets a trusted identity token issuer.
  
## See also

#### 

[Set-SPTrustedIdentityTokenIssuer](set-sptrustedidentitytokenissuer.md)
  
[New-SPTrustedIdentityTokenIssuer](new-sptrustedidentitytokenissuer.md)
  
[Remove-SPTrustedIdentityTokenIssuer](remove-sptrustedidentitytokenissuer.md)

