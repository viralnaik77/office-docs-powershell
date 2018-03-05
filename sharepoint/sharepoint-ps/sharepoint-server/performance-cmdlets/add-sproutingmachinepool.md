---
title: "Add-SPRoutingMachinePool"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bcd04aa7-924b-4308-bac1-04e5750aa503

description: "Adds a new machine pool."
---

# Add-SPRoutingMachinePool

Adds a new machine pool.
  
```
Add-SPRoutingMachinePool [-RequestManagementSettings] <SPRequestManagementSettingsPipeBind> [-Name] <String> [-AssignmentCollection <SPAssignmentCollection>] [-MachineTargets <SPRoutingRuleTargetPipeBind[]>]
```

## Detailed Description

Use the **Add-SPRoutingMachinePool** cmdlet to add a machine pool by using the **RequestManagementSettings** and **Name** parameters. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**RequestManagementSettings** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementSettingsPipeBind  <br/> |Specifies the name of the request management settings object to add to the routing machine pool.  <br/> |
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of machine pool.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**MachineTargets** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingRuleTargetPipeBind[]  <br/> |Specifies the routing targets collection that the machine pool will contain.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**RequestManagementSettings** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementSettingsPipeBind  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**MachineTargets** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingRuleTargetPipeBind[]  <br/> ||
   
## Example

----------EXAMPLE--------
  
```
$web=Get-SPWebApplication -Identity <URL of web application>
```

```
$rm=Get-SPRequestManagementSettings -Identity $web
```

```
Add-SPRoutingMachinePool -RequestManagementSettings $rm -Name <MachineName>
```

This example adds a machine pool.
  
## See also

#### 

[Get-SPRoutingMachinePool](get-sproutingmachinepool.md)
  
[Remove-SPRoutingMachinePool](remove-sproutingmachinepool.md)
  
[Set-SPRoutingMachinePool](set-sproutingmachinepool.md)

