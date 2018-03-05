---
title: "Get-SPPendingUpgradeActions"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/5/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c91abe03-67a6-4e7d-a3ff-5f7a81620382

description: "Displays pending upgrade actions."
---

# Get-SPPendingUpgradeActions

Displays pending upgrade actions.
  
```
Get-SPPendingUpgradeActions -RootObject <IUpgradable> [-AssignmentCollection <SPAssignmentCollection>] [-Recursive <SwitchParameter>] [-SkipSiteUpgradeActionInfo <SwitchParameter>]

```

## Example

-----------EXAMPLE-------
  
```
Get-SPFarm | Get-SPPendingUpgradeActions -Recursive
```

## Detailed Description

Use the **Get-SPPendingUpgradeActions** cmdlet to display the current pending upgrade actions for the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _RootObject_ <br/> |Required  <br/> |Microsoft.SharePoint.Administration.IUpgradable  <br/> |Specifies a SharePoint object where you check for which upgrade actions are outstanding for that object based on its current upgrade status. This object must be inherited from IUpgradable.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Recursive_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether to perform the same pending upgrade action checks on each IUpgradable object that occurs under the **RootObject** parameter that is specified.  <br/> |
| _SkipSiteUpgradeActionInfo_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to not include pending upgrade actions for all child objects of a content database.  <br/> |
   

