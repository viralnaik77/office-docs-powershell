---
title: "Upgrade-SPSite"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3dc2f4ae-8ca1-4912-94ea-93c8b6cdd096

description: "Starts the upgrade process on a site collection."
---

# Upgrade-SPSite

Starts the upgrade process on a site collection.
  
```
Upgrade-SPSite -Identity <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Email <SwitchParameter>] [-Priority <Byte>] [-QueueOnly <SwitchParameter>] [-Unthrottled <SwitchParameter>] [-VersionUpgrade <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

-------------EXAMPLE 1---------- 
  
```
Upgrade-SPSite http://<site name>/sites/testsite
```

This example upgrades the existing http://\<site name\>/sites/testsite site collection by using only build-to-build upgrade actions. The SPSite.CompatibilityLevel will not be changed by this operation.
  
-------------EXAMPLE 2---------- 
  
```
Upgrade-SPSite http://<site name>/sites/testsite -VersionUpgrade
```

This example upgrades the existing http://\<site name\>/sites/testsite site collection by using only build-to-build upgrade actions. The SPSite.CompatibilityLevel will not be changed by this operation.
  
## Detailed Description

The **Upgrade-SPSite** cmdlet starts the upgrade process on a site collection. 
  
The **Upgrade-SPSite** cmdlet activates the upgrade process for the specified **SPSite** object. You can also use this cmdlet to resume failed upgrades. When you use this cmdlet to initiate upgrade on an **SPSite** object, the object can be either a build-to-build or version-to-version upgrade. By default, the **Upgrade-SPSite** cmdlet operates as a build-to-build upgrade. This prevents unexpected version upgrades of site collections if you use this cmdlet after a patching operation. When in version-to-version upgrade mode, site collection health checks are run in repair mode to ensure that the site collection is healthy enough to upgrade successfully. If successful, the remainder of the upgrade occurs. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the **SPSite** object to run upgrade operations against.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Email_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether to send mail on completion of the site collection upgrade.  <br/> |
| _Priority_ <br/> |Optional  <br/> |System.Byte  <br/> | Specifies what priority to upgrade the site.  <br/>  The valid values are:  <br/>  128 - 255 (Low Priority)  <br/>  11 - 127 (Normal Priority)  <br/>  0 - 10 (High Priority)  <br/> |
| _QueueOnly_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to put the site into the queue for a delayed upgrade that is managed by a timer job  <br/> |
| _Unthrottled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies a farm administrator to bypass the throttle which permits a site collection to be upgraded even if there are "too many" site collections in the throttle to be upgraded.  <br/> |
| _VersionUpgrade_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to perform a version-to-version upgrade on the **SPSite** object. When this parameter is set, it internally triggers all available build-to-build actions that are associated with the current site collection operating mode. Version-to-version actions follow to bring site collections to the next site collection operating mode inclusive of all new build-to-build actions that are associated with the new site collection operating mode. When this parameter is not set, it triggers only available build-to-build upgrade actions that are associated with the current site collection operating mode.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   

