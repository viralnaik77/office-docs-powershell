---
title: "Get-SPBingMapsBlock"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39896775-2736-46f0-98cb-c91244a99ce9

description: "Returns Bing Maps blocked status."
---

# Get-SPBingMapsBlock

Returns Bing Maps blocked status.
  
```
Get-SPBingMapsBlock [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Get-SPBingMapsBlock** cmdlet to return true or false on whether Bing Maps are blocked in all locales. This cmdlet will return an object, and "BlockBingMapsInAllLocales" property will return True or False. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-----------EXAMPLE-----------
  
```
Get-SPBingMapsBlock
```

This example returns an object, and **BlockBingMapsInAllLocales** property will return True or False on whether Bing Maps are blocked in all locales. 
  
## See also

#### 

[Set-SPBingMapsBlock](set-spbingmapsblock.md)
  
[Get-SPBingMapsKey](get-spbingmapskey.md)
  
[Set-SPBingMapskey](set-spbingmapskey.md)

