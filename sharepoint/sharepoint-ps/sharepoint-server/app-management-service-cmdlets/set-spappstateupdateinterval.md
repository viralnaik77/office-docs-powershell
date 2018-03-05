---
title: "Set-SPAppStateUpdateInterval"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14314f7a-c930-466f-839b-0586a556d905

description: "Sets the interval in hours between updates of the app state update job."
---

# Set-SPAppStateUpdateInterval

Sets the interval in hours between updates of the app state update job.
  
```
Set-SPAppStateUpdateInterval -AppStateSyncHours <Int32> -FastAppRevocationHours <Int32> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Set-SPAppStateUpdateInterval** cmdlet to set the interval in hours between updates of the app state update job. The app state update job updates the app states, including app updates, in SharePoint Server 2016 based on information in the SharePoint Store . 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppStateSyncHours** <br/> |Required  <br/> |System.Int32  <br/> |Specifies the interval in hours between updates of the app states. Values are 1 to 24 inclusive.  <br/> |
|**FastAppRevocationHours** <br/> |Required  <br/> |System.Int32  <br/> |Specifies the interval in hours between checks of the list of revoked apps in the SharePoint Store. If the list of revoked apps has changed from the last time, the app states are updated.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppStateSyncHours** <br/> |Required  <br/> |System.Int32  <br/> ||
|**FastAppRevocationHours** <br/> |Required  <br/> |System.Int32  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-------------EXAMPLE--------------
  
```
Set-SPAppStateUpdateInterval -AppStateSyncHours 24 -FastAppRevocationHours 6
```

This example sets the app state update interval to 24 hours and the fast app revocation interval to 6 hours.
  
## See also

#### 

[Get-SPAppStateUpdateInterval](get-spappstateupdateinterval.md)

