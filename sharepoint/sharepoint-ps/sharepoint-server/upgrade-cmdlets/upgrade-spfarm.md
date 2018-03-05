---
title: "Upgrade-SPFarm"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 56061db1-1e9a-40c1-9015-7e38a3cda20e

description: "Activates the Upgrade method for the local farm."
---

# Upgrade-SPFarm

Activates the Upgrade method for the local farm.
  
```
Upgrade-SPFarm [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-ServerOnly <SwitchParameter>] [-SkipDatabaseUpgrade <SwitchParameter>] [-SkipSiteUpgrade <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

-----------EXAMPLE--------- 
  
```
Upgrade-SPFarm
```

This example starts the upgrade process on the local farm.
  
## Detailed Description

The **Upgrade-SPFarm** cmdlet starts the upgrade process on the local farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _ServerOnly_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to only upgrade local server.  <br/> |
| _SkipDatabaseUpgrade_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to not upgrade databases and their child objects when performing upgrade.  <br/> |
| _SkipSiteUpgrade_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to not upgrade all site objects when performing upgrade.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   

