---
title: "Remove-SPRoutingRule"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 609d6620-8c86-4fbf-a07d-c3334a232916

description: "Removes a routing rule."
---

# Remove-SPRoutingRule

Removes a routing rule.
  
```
Remove-SPRoutingRule [-Identity] <SPRoutingRulePipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Remove-SPRoutingRule** cmdlet removes a routing rule by using the **Identity** parameter. If the **Identity** parameter is not specified, the routing rules for the entire farm are removed. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingRulePipeBind  <br/> |Specifies the rule object to remove.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingRulePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------EXAMPLE----------
  
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
$c=New-SPRequestManagementRuleCriteria -Value http -Property url -MatchType startswith -CaseSensitive $false
```

```
$rule=Add-SPRoutingRule -RequestManagementSettings $rm -Name <Rule Name> -Criteria $c -MachinePool $pool
```

```
Remove-SPRoutingRule -Identity $rule
```

This example removes a routing for a specified identity by using the **$rule** variable. 
  
## See also

#### 

[Add-SPRoutingRule](add-sproutingrule.md)
  
[Get-SPRoutingRule](get-sproutingrule.md)
  
[Set-SPRoutingRule](set-sproutingrule.md)

