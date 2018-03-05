---
title: "Remove-SPClaimProvider"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0633eeaf-94b3-40dc-9750-2aa83ac09247

description: "Unregisters a claim provider."
---

# Remove-SPClaimProvider

Unregisters a claim provider.
  
```
Remove-SPClaimProvider [-Identity] <SPClaimProviderPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Remove-SPClaimProvider** cmdlet unregisters a claim provider. If the unregistered claim provider was assigned to a trusted identity token issuer, the trusted token issuer will use the default (system) claim provider. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPClaimProviderPipeBind  <br/> |Specifies the claim provider to unregister.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a claim provider (for example, MyClaimProvider1); or an instance of a valid **SPClaimProvider** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPClaimProviderPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Remove - SPClaimProvider -Identity "12345678-90ab-cdef-1234-567890bcdefgh"
```

This example removes a claim provider from the farm
  
## See also

#### 

[Get-SPClaimProvider](get-spclaimprovider.md)
  
[New-SPClaimProvider](new-spclaimprovider.md)
  
[Set-SPClaimProvider](set-spclaimprovider.md)

