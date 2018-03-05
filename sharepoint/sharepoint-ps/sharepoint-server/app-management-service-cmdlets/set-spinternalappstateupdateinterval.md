---
title: "Set-SPInternalAppStateUpdateInterval"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b09a7e1b-7ca1-42a7-8660-384c0e3d7a28

description: "Sets the interval in hours between updates of the internal app state update job."
---

# Set-SPInternalAppStateUpdateInterval

Sets the interval in hours between updates of the internal app state update job.
  
```
Set-SPInternalAppStateUpdateInterval -AppStateSyncHours <Int32> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Set-SPInternalAppStateUpdateInterval** cmdlet to set the interval in hours between updates of the internal app state update job. The internal app state update job gets app upgrades from the internal app directory and sets them on app instances. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppStateSyncHours** <br/> |Required  <br/> |System.Int32  <br/> |Specifies the hour for which the internal app states are updated.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

-------------EXAMPLE------------
  
```
Set-SPInternalAppStateUpdateInterval -AppStateSyncHours 24
```

This example sets a 24-hour interval between updates of the internal app state update job.
  
## See also

#### 

[Get-SPInternalAppStateUpdateInterval](get-spinternalappstateupdateinterval.md)

