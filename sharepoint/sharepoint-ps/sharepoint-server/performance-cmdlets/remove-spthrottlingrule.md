---
title: "Remove-SPThrottlingRule"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfc09a8e-89c1-4d67-98c9-82f94ec32a5b

description: "Removes a throttling rule."
---

# Remove-SPThrottlingRule

Removes a throttling rule.
  
```
Remove-SPThrottlingRule [-Identity] <SPThrottlingRulePipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Remove-SPThrottlingRule** cmdlet to remove a throttling rule from the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPThrottlingRulePipeBind  <br/> |Specifies the throttling rule object to remove.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPThrottlingRulePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------EXAMPLE-------
  
```
$web=Get-SPWebApplication -Identity <URL of web application>
```

```
$rm=Get-SPRequestManagementSettings -Identity $web
```

```
$c=New-SPRequestManagementRuleCriteria -Value http -Property url -MatchType startswith -CaseSensitive $false
```

```
$throttlingrule=Add-SPThrottlingRule -RequestManagementSettings $rm -Name <Rule Name> -Criteria $c -Threshold 4
```

```
Remove-SPThrottlingRule -Identity $throttlingrule
```

This example removes a throttling rule for a specified identity by using the **$throttlingrule** variable. 
  
## See also

#### 

[Add-SPThrottlingRule](add-spthrottlingrule.md)
  
[Get-SPThrottlingRule](get-spthrottlingrule.md)
  
[Set-SPThrottlingRule](set-spthrottlingrule.md)

