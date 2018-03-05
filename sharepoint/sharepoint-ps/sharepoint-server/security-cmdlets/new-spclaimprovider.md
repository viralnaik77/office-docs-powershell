---
title: "New-SPClaimProvider"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3183078d-7ea9-49b9-b408-4bac92c4a72d

description: "Registers a new claim provider in the farm."
---

# New-SPClaimProvider

Registers a new claim provider in the farm.
  
```
New-SPClaimProvider -AssemblyName <String> -Description <String> -DisplayName <String> -Type <String> [-AssignmentCollection <SPAssignmentCollection>] [-Default <SwitchParameter>] [-Enabled <SwitchParameter>]
```

## Detailed Description

The **New-SPClaimProvider** cmdlet registers a new claim provider in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssemblyName** <br/> |Required  <br/> |System.String  <br/> |The type must be a valid name of an assembly; for example, ClaimAssembly1.  <br/> Specifies the name of the assembly with the claim provider.  <br/> |
|**Description** <br/> |Required  <br/> |System.String  <br/> |Specifies the description of the claim provider.  <br/> The type must be a valid name of an assembly; for example, ClaimAssembly1.  <br/> |
|**DisplayName** <br/> |Required  <br/> |System.String  <br/> |Specifies the display name of the new claim provider.  <br/> The type must be a valid name of a claim provider; for example, ClaimProvider1.  <br/> |
|**Type** <br/> |Required  <br/> |System.String  <br/> |Specifies the type of the claim.  <br/> The type must be a valid name of a claim type; for example MyClaimProvider.Providers.CustomProvider.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Default** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the claim provider applies to all Web applications and zones.  <br/> |
|**Enabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Turns on the claim provider.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssemblyName** <br/> |Required  <br/> |System.String  <br/> ||
|**Description** <br/> |Required  <br/> |System.String  <br/> ||
|**DisplayName** <br/> |Required  <br/> |System.String  <br/> ||
|**Type** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Default** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Enabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1------------------
  
```
New-SPClaimProvider -Name "MyClaimProvider" -Type "MyClaimProvider.Providers.CustomProvider" -AllWebApplications
```

This example registers a claim provider in the farm.
  
------------------EXAMPLE 2------------------
  
```
New-SPClaimProvider -Name "MyClaimProvider" -Type "MyClaimProvider.Providers.CustomProvider" -Scope (Get-SPWebApplication http://test)
```

This example registers a claim provider scoped to a given Web application.
  
## See also

#### 

[Get-SPClaimProvider](get-spclaimprovider.md)
  
[Set-SPClaimProvider](set-spclaimprovider.md)
  
[Remove-SPClaimProvider](remove-spclaimprovider.md)

