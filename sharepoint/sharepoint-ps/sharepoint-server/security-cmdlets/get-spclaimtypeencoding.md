---
title: "Get-SPClaimTypeEncoding"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea6de2b0-d45e-455c-b393-67c9b3136ba4

description: "Returns a list of all the types of claims."
---

# Get-SPClaimTypeEncoding

Returns a list of all the types of claims.
  
```
Get-SPClaimTypeEncoding [-AssignmentCollection <SPAssignmentCollection>] [-ClaimType <String>] [-EncodingCharacter <Char>]
```

## Detailed Description

Use the **Get-SPClaimTypeEncoding** cmdlet to return the following: 
  
- A list of all the types of claims that are registered in the farm
    
- The Unicode character that will be encoded when the SPClaim.ToEncodedString method is invoked
    
- The SPClaim.ClaimType property is set to a valid value
    
For additional information about the SPClaim methods and properties, see [ToEncodedString()](https://msdn.microsoft.com/library/Microsoft.SharePoint.Administration.Claims.SPClaim.ToEncodedString.aspx) and [ClaimType()](https://msdn.microsoft.com/library/Microsoft.SharePoint.Administration.Claims.SPClaim.ClaimType.aspx) respectively. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**ClaimType** <br/> |Optional  <br/> |System.String  <br/> |Specifies an encoding character that is mapped to a type of input claim.  <br/> |
|**EncodingCharacter** <br/> |Optional  <br/> |System.Char  <br/> |Specifies a type of claim that is mapped to an input character.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**ClaimType** <br/> |Optional  <br/> |System.String  <br/> ||
|**EncodingCharacter** <br/> |Optional  <br/> |System.Char  <br/> ||
   
## Example

--------------EXAMPLE 1-------- 
  
```
Get-SPClaimTypeEncoding
```

This example returns a list of all types of claima in the farm.
  
--------------EXAMPLE 2-------- 
  
```
Get-SPClaimTypeEncoding -ClaimType "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/country"
```

This example returns a specific claim type by using the **ClaimType** parameter. 
  
## See also

#### 

[New-SPClaimTypeEncoding](new-spclaimtypeencoding.md)

