---
title: "Add-SPThrottlingRule"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 6/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4e745a64-d91d-4887-a5a9-1000f5dfaf40

description: "Adds a new throttling rule."
---

# Add-SPThrottlingRule

Adds a new throttling rule.
  
```
Add-SPThrottlingRule -Name <String> -RequestManagementSettings <SPRequestManagementSettingsPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Criteria <SPRequestManagementRuleCriteriaPipeBind[]>] [-Expiration <DateTime>] [-Threshold <Int32>]

```

## Example

-----------EXAMPLE---------
  
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
Add-SPThrottlingRule -RequestManagementSettings $rm -Name <Rule Name> -Criteria $c -Threshold 4
```

This example adds a throttling rule for a specified identity by using the **$rm** and **$c** variables. 
  
## Detailed Description

The **Add-SPThrottlingRule** cmdlet adds a new throttling rule for the farm by using the **Name** and **RequestManagementSettings** parameters. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the throttling rule.  <br/> |
| _RequestManagementSettings_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementSettingsPipeBind  <br/> |Specifies the name of the request management settings object to add.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Criteria_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementRuleCriteriaPipeBind[]  <br/> |Specifies the criteria for the rule to match.  <br/> |
| _Expiration_ <br/> |Optional  <br/> |System.DateTime  <br/> |Specifies the expiration date and time of the rule.  <br/> |
| _Threshold_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies a value between 0 and 10 which defines the maximum threshold for throttling. The Request Manager will remove routing targets if their Health-Score becomes greater than this value.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**RequestManagementSettings** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementSettingsPipeBind  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Criteria** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementRuleCriteriaPipeBind[]  <br/> ||
|**Expiration** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Threshold** <br/> |Optional  <br/> |System.Nullable  <br/> ||
   
## See also

#### 

[Get-SPThrottlingRule](get-spthrottlingrule.md)
  
[Remove-SPThrottlingRule](remove-spthrottlingrule.md)
  
[Set-SPThrottlingRule](set-spthrottlingrule.md)

