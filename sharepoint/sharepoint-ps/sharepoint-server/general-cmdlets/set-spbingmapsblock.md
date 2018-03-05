---
title: "Set-SPBingMapsBlock"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b941b884-71c1-4cd2-b2b3-635d1b6f27b2

description: "Sets Bing maps to blocked status."
---

# Set-SPBingMapsBlock

Sets Bing maps to blocked status.
  
```
Set-SPBingMapsBlock [[-BlockBingMapsInAllLocales] <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Set-SPBingMapsBlock** cmdlet to specify whether to block Bing Maps in all locales, or not to block them in all locales. Bing Maps will be displayed only in non-restricted locales if this property is not set. The default value is 0 (not blocked). Use a value of 1 to block in all locales. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**BlockBingMapsInAllLocales** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether Bing Maps are blocked in all locales.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**BlockBingMapsInAllLocales** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-------------EXAMPLE----------
  
```
Set-SPBingMapsBlock 1
```

This example displays how to block Bing Maps in all locales for the farm.
  
## See also

#### 

[Get-SPBingMapsBlock](get-spbingmapsblock.md)
  
[Get-SPBingMapsKey](get-spbingmapskey.md)
  
[Set-SPBingMapskey](set-spbingmapskey.md)

