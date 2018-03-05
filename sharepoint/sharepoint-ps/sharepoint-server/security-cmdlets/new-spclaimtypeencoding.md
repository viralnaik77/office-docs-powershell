---
title: "New-SPClaimTypeEncoding"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5995cda3-c97e-4317-8fc9-84bc5b63b9a2

description: "Registers a new type of claim."
---

# New-SPClaimTypeEncoding

Registers a new type of claim.
  
```
New-SPClaimTypeEncoding -ClaimType <String> -EncodingCharacter <Char> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **New-SPClaimTypeEncoding** cmdlet to register the following: 
  
- A new type of claim
    
- The Unicode character to which it should be encoded when the SPClaim.ToEncodedString method is invoked
    
- The SPClaim.ClaimType property is set to a valid value
    
For more information about the SPClaim methods and properties, see [ToEncodedString()](https://msdn.microsoft.com/library/Microsoft.SharePoint.Administration.Claims.SPClaim.ToEncodedString.aspx) and [ClaimType()](https://msdn.microsoft.com/library/Microsoft.SharePoint.Administration.Claims.SPClaim.ClaimType.aspx) respectively. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ClaimType** <br/> |Required  <br/> |System.String  <br/> |Specifies the type of claim for which you want to create a mapping.  <br/> |
|**EncodingCharacter** <br/> |Required  <br/> |System.Char  <br/> |Specifies the Unicode character to which you want to create a mapping.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Suppresses confirmation messages to any claim type that is added.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ClaimType** <br/> |Required  <br/> |System.String  <br/> ||
|**EncodingCharacter** <br/> |Required  <br/> |System.Char  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Suppresses any dialog box that is displayed.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------EXAMPLE------- 
  
```
New-SPClaimTypeEncoding -EncodingCharacter '1' -ClaimType "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/country"
```

This example registers a new type of claim.
  
## See also

#### 

[Get-SPClaimTypeEncoding](get-spclaimtypeencoding.md)

