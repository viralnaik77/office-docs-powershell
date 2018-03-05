---
title: "Set-SPRoutingRule"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 6/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db685b78-a3c4-4cd4-a746-80d54598b474

description: "Changes properties of an existing routing rule."
---

# Set-SPRoutingRule

Changes properties of an existing routing rule.
  
```
Set-SPRoutingRule -Identity <SPRoutingRulePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Criteria <SPRequestManagementRuleCriteriaPipeBind[]>] [-ExecutionGroup <Int32>] [-Expiration <DateTime>] [-MachinePool <SPRoutingMachinePoolPipeBind>]

```

## Example

------------EXAMPLE---------
  
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
$pool=Add-SPRoutingMachinePool -RequestManagementSettings $rm -Name <Name of Pool> -MachineTargets $machines
```

```
$criteria=New-SPRequestManagementRuleCriteria -Value http -Property url -MatchType startswith -CaseSensitive $false
```

```
$rule=Add-SPRoutingRule -RequestManagementSettings $rm -Name <Rule Name> -Criteria $c -MachinePool $pool
```

```
$criteriaNew = New-SPRequestManagementRuleCriteria -Property UserAgent -MatchType Equals -Value "Mozilla/4.0 (compatible; MSIE 4.01; Windows NT; MS Search 6.0 Robot)"
```

```
Set-SPRoutingRule -Identity $rule -Criteria $criteriaNew
```

This example sets a routing rule for the specified identity by using the **$rule** variable. 
  
## Detailed Description

Use the **Set-SPRoutingRule** cmdlet to change properties of an existing routing rule. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingRulePipeBind  <br/> |Specifies the name of the request management settings object to set.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Criteria_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementRuleCriteriaPipeBind[]  <br/> |Specifies the criteria for the rule to match.  <br/> |
| _ExecutionGroup_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the group in which the rule will be placed.  <br/> |
| _Expiration_ <br/> |Optional  <br/> |System.DateTime  <br/> |Specifies the expiration date and time of the rule.  <br/> |
| _MachinePool_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingMachinePoolPipeBind  <br/> |Specifies the pool of machines to which a request will be routed if the changed rule is matched.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingRulePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Criteria** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementRuleCriteriaPipeBind[]  <br/> ||
|**ExecutionGroup** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Expiration** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MachinePool** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingMachinePoolPipeBind  <br/> ||
   
## See also

#### 

[Add-SPRoutingRule](add-sproutingrule.md)
  
[Get-SPRoutingRule](get-sproutingrule.md)
  
[Remove-SPRoutingRule](remove-sproutingrule.md)

