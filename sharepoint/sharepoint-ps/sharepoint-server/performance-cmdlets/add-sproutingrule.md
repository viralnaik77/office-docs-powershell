---
title: "Add-SPRoutingRule"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 6/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6ccf7b7b-4615-4693-93a3-37f2502c796d

description: "Adds a routing rule."
---

# Add-SPRoutingRule

Adds a routing rule.
  
```
Add-SPRoutingRule -Name <String> -RequestManagementSettings <SPRequestManagementSettingsPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Criteria <SPRequestManagementRuleCriteriaPipeBind[]>] [-ExecutionGroup <Int32>] [-Expiration <DateTime>] [-MachinePool <SPRoutingMachinePoolPipeBind>]

```

## Example

--------------EXAMPLE--------
  
```
$rm=Get-SPRequestManagementSettings -Identity $web
```

```
Get-SPRoutingRule -RequestManagementSettings $rm
```

```
$machines=Get-SPRoutingMachineInfo -RequestManagementSettings $rm
```

```
Add-SPRoutingMachinePool -RequestManagementSettings $rm -Name <Name of Pool> -MachineTargets $machines
```

This examples adds a routing rule to the farm by using the **$rm** and **$machines** variables. 
  
## Detailed Description

The **Add-SPRoutingRule** cmdlet adds a routing rule for the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the rule.  <br/> |
| _RequestManagementSettings_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementSettingsPipeBind  <br/> |Specifies the name of the request management settings object to add to the routing rule.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Criteria_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementRuleCriteriaPipeBind[]  <br/> |Specifies the criteria for the rule to match.  <br/> |
| _ExecutionGroup_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the group in which the rule will be placed.  <br/> |
| _Expiration_ <br/> |Optional  <br/> |System.DateTime  <br/> |Specifies the expiration date and time of the rule.  <br/> |
| _MachinePool_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingMachinePoolPipeBind  <br/> |Specifies the pool of machines to which a request will be routed if the created rule is matched.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**RequestManagementSettings** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementSettingsPipeBind  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Criteria** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementRuleCriteriaPipeBind[]  <br/> ||
|**ExecutionGroup** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Expiration** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MachinePool** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingMachinePoolPipeBind  <br/> ||
   
## See also

#### 

[Get-SPRoutingRule](get-sproutingrule.md)
  
[Remove-SPRoutingRule](remove-sproutingrule.md)
  
[Set-SPRoutingRule](set-sproutingrule.md)

