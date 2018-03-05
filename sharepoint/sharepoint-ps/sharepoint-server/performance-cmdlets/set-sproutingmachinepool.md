---
title: "Set-SPRoutingMachinePool"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52826663-4a9e-461f-8610-66a54ecc7b6a

description: "Sets properties of a machine pool."
---

# Set-SPRoutingMachinePool

Sets properties of a machine pool.
  
```
Set-SPRoutingMachinePool [-Identity] <SPRoutingMachinePoolPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-MachineTargets <SPRoutingRuleTargetPipeBind[]>]
```

## Detailed Description

Use the **Set-SPRoutingMachinePool** cmdlet to set properties of a machine pool by using the **Identity** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingMachinePoolPipeBind  <br/> |Specifies the name of the request management settings object to set.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**MachineTargets** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingRuleTargetPipeBind[]  <br/> |Specifies the routing targets collection that the machine pool will contain.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingMachinePoolPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**MachineTargets** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingRuleTargetPipeBind[]  <br/> ||
   
## Example

```
$web=Get-SPWebApplication -Identity <URL of web application>
```

```
$rm=Get-SPRequestManagementSettings -Identity $web
```

```
$pool=Get-SPRoutingMachinePool -RequestManagementSettings $rm
```

```
Set-SPRoutingMachinePool -Identity $pool -MachineTargets <Machine collections>
```

This example sets the machine pool property of **MachineTargets** for a specified identity as defined by the **$pool** variable. 
  
## See also

#### 

[Add-SPRoutingMachinePool](add-sproutingmachinepool.md)
  
[Get-SPRoutingMachinePool](get-sproutingmachinepool.md)
  
[Remove-SPRoutingMachinePool](remove-sproutingmachinepool.md)

