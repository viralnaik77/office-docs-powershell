---
title: "Set-SPSecureStoreDefaultProvider"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe43afc-cf09-4c98-baa6-96a81c2aaa06

description: "Updates the secure store provider."
---

# Set-SPSecureStoreDefaultProvider

Updates the secure store provider.
  
```
Set-SPSecureStoreDefaultProvider -Type <Type> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Set-SPSecureStoreDefaultProvider** cmdlet sets or replaces the secure store provider. To register a third-party secure store, implement the **ISecureStoreProvider** interface. With the interface defined, place the DLL file in the global assembly cache, and then load the DLL and load the type, as shown in the example. You can then set the secure store provider. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Type** <br/> |Required  <br/> |System.Type  <br/> |
> Specifies the provider type. The type must be loaded in memory.

The type must be a secure store provider type enclosed in square brackets; for example, [Reflection.Assembly].  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Type** <br/> |Required  <br/> |System.Type  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
[Reflection.Assembly]::LoadFrom("C:\ContosoFolder\contosoSecureStore.dll")
```

```
$type = [Contoso.SecureStore.ContosoSecureStoreProvider]
```

```
Set-SPSecureStoreDefaultProvider -Type $type
```

This example sets the custom implemented secure store provider.
  

