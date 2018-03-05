---
title: "New-SPUserSettingsProvider"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a1075c31-6b45-4696-aee8-d48316f027ef

description: "Adds a new User Settings Provider."
---

# New-SPUserSettingsProvider

Adds a new User Settings Provider.
  
```
New-SPUserSettingsProvider -AssemblyName <String> -DisplayName <String> -Type <String> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **New-SPUserSettingsProvider** cmdlet to add a new User Settings Provider to the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssemblyName** <br/> |Required  <br/> |System.String  <br/> |Specifies the assembly name for the provider.  <br/> |
|**DisplayName** <br/> |Required  <br/> |System.String  <br/> |Specifies the display name to use for this provider.  <br/> |
|**Type** <br/> |Required  <br/> |System.String  <br/> |Specifies the type name to use for this provider.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssemblyName** <br/> |Required  <br/> |System.String  <br/> ||
|**DisplayName** <br/> |Required  <br/> |System.String  <br/> ||
|**Type** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-----------EXAMPLE-------
  
```
New-SPUserSettingsProvider -DisplayName "My User Settings Provider" -AssemblyName MyProvider.dll -Type MyProvider
```

This example adds a user setting provider with a display name of "My User Settings Provider" which uses the MyProvider.dll file.
  
## See also

#### 

[Get-SPUserSettingsProvider](get-spusersettingsprovider.md)
  
[Remove-SPUserSettingsProvider](remove-spusersettingsprovider.md)
  
[Get-SPUserSettingsProviderManager](get-spusersettingsprovidermanager.md)

