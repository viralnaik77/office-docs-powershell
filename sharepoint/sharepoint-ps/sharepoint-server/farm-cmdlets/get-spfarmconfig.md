---
title: "Get-SPFarmConfig"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83a26555-6b6e-4959-9a6a-bdef049de2a2

description: "Returns a global property or a collection of global properties for the local farm."
---

# Get-SPFarmConfig

Returns a global property or a collection of global properties for the local farm.
  
```
Get-SPFarmConfig [-AssignmentCollection <SPAssignmentCollection>] [-ServiceConnectionPoint <SwitchParameter>]
```

## Detailed Description

The **Get-SPFarmConfig** cmdlet retrieves global settings for the local farm that are not members of the **SPFarm** object. This cmdlet creates a new **PSCustomObject** object from the collection of properties returned from the local farm, and then adds this object to the pipeline. The **PSCustomObject** object can be read, or modified and passed to the **Set-SPFarmConfig** cmdlet to change parameter values. 
  
The properties collected in the **PSCustomObject** object must be farm-wide settings, and must be configurable only once for the entire farm. The parameter name added to the **PSCustomObject** object must match exactly the input parameter name for the **Set-SPFarmConfig** cmdlet. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**ServiceConnectionPoint** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Gets the information stored in the current farm's service connection point in Active Directory.  <br/> |
   
## Example

-------------EXAMPLE----------------
  
```
$a = Get-SPFarmConfig
```

```
$a.AjaxTimeout = 200
```

```
$a | Set-SPFarmConfig
```

This example uses the  `Get-SPFarmConfig` cmdlet to add the  `Ajax Timeout` setting to the **PSCustomObject** object, sets the value for  `Ajax Timeout`, and then passes **PSCustomObject** to the **Set-SPFarmConfig** cmdlet to change the  `Ajax Timeout` setting.  `Ajax Timeout`, a farm-wide setting, is a member of the **SPWebService** object and cannot be accessed with a Windows PowerShell cmdlet. 
  
You can perform the same operations with either of the following commands.
  
```
Set-SPFarmConfig -AjaxTimeout 200
```

```
Get-SPFarmConfig | Select AjaxTimeout 200
```

## See also

#### 

[Set-SPFarmConfig](set-spfarmconfig.md)

