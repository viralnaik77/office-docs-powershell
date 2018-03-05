---
title: "Remove-SPTrustedServiceTokenIssuer"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 147712f5-7074-4f63-b4e8-de0f8d51b28e

description: "Deletes the object that represents the farm trust."
---

# Remove-SPTrustedServiceTokenIssuer

Deletes the object that represents the farm trust.
  
```
Remove-SPTrustedServiceTokenIssuer [-Identity] <SPTrustedServiceTokenIssuerPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPTrustedServiceTokenIssuer** cmdlet deletes the object that represents the farm trust. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedServiceTokenIssuerPipeBind  <br/> |Specifies the trusted service token issuer to delete.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a trusted service token issuer (for example, WFEFarm1); or an instance of a valid **SPTrustedRootAuthority** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedServiceTokenIssuerPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Remove-SPTrustedServiceTokenIssuer "WFE Farm 2"
```

This example deletes the trusted service token issuer  `WFE Farm 2`.
  
## See also

#### 

[Set-SPTrustedServiceTokenIssuer](set-sptrustedservicetokenissuer.md)
  
[New-SPTrustedServiceTokenIssuer](new-sptrustedservicetokenissuer.md)
  
[Get-SPTrustedServiceTokenIssuer](get-sptrustedservicetokenissuer.md)

