---
title: "Remove-SPTrustedIdentityTokenIssuer"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5863a758-d62e-4208-a19f-5bd012671ee7

description: "Deletes a Security Token Service (STS) identity provider from the farm."
---

# Remove-SPTrustedIdentityTokenIssuer

Deletes a Security Token Service (STS) identity provider from the farm.
  
```
Remove-SPTrustedIdentityTokenIssuer [-Identity] <SPTrustedIdentityTokenIssuerPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPTrustedIdentityTokenIssuer** cmdlet deletes a Security Token service (STS) identity provider from the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> |Specifies the identity provider to remove.  <br/> The type must be one of the following forms:  <br/> --A valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh  <br/> --A valid name of identity provider (for example, LiveID STS)  <br/> --An instance of a valid **SPIdentityProvider** object  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE--------------------
  
```
Remove-SPTrustedIdentityTokenIssuer "LiveIDSTS"
```

This example removes an identity provider named  `LiveIDSTS` from the farm. 
  
## See also

#### 

[Get-SPTrustedIdentityTokenIssuer](get-sptrustedidentitytokenissuer.md)
  
[Set-SPTrustedIdentityTokenIssuer](set-sptrustedidentitytokenissuer.md)
  
[New-SPTrustedIdentityTokenIssuer](new-sptrustedidentitytokenissuer.md)

