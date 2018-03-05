---
title: "Remove-SPUserSettingsProvider"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e0bb0a7f-7949-4a4b-952a-bc0749813394

description: "Removes a User Settings Provider."
---

# Remove-SPUserSettingsProvider

Removes a User Settings Provider.
  
```
Remove-SPUserSettingsProvider [-Identity] <SPUserSettingsProviderPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Remove-SPUserSettingsProvider** cmdlet to remove a User Settings Provider from the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserSettingsProviderPipeBind  <br/> |Specifies the GUID ID for a User Settings Provider to remove.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserSettingsProviderPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-----------EXAMPLE--------
  
```
Remove-SPUserSettingsProvider -Identity "234bf0ed-70db-4158-a332-4dfd683b4148"
```

This example removes a specific User Settings Provider by using the GUID, 234bf0ed-70db-4158-a332-4dfd683b4148.
  
## See also

#### 

[Get-SPUserSettingsProvider](get-spusersettingsprovider.md)
  
[New-SPUserSettingsProvider](new-spusersettingsprovider.md)
  
[Get-SPUserSettingsProviderManager](get-spusersettingsprovidermanager.md)

