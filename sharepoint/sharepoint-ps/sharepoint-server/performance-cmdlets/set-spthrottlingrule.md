---
title: "Set-SPThrottlingRule"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 6/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55331a1c-fa51-4018-a31a-8ab928eebc20

description: "Changes properties of an existing throttling rule."
---

# Set-SPThrottlingRule

Changes properties of an existing throttling rule.
  
```
Set-SPThrottlingRule -Identity <SPThrottlingRulePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Criteria <SPRequestManagementRuleCriteriaPipeBind[]>] [-Expiration <DateTime>] [-Threshold <Int32>]

```

## Example

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
$criteriaNew = New-SPRequestManagementRuleCriteria -Property UserAgent -MatchType Equals -Value "Mozilla/4.0 (compatible; MSIE 4.01; Windows NT; MS Search 6.0 Robot)"
```

```
Set-SPThrottlingRule -Identity $ throttlingrule -Criteria $criteriaNew -Threshold 8
```

This example sets throttling rule property 
  
## Detailed Description

Use the **Set-SPThrottlingRule** cmdlet to change the properties of an existing throttling rule by using the **Identity** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPThrottlingRulePipeBind  <br/> |Specifies the throttling rule object to set.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Criteria_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementRuleCriteriaPipeBind[]  <br/> |Specifies the criteria for the rule to match.  <br/> |
| _Expiration_ <br/> |Optional  <br/> |System.DateTime  <br/> |Specifies the expiration date and time of the rule.  <br/> |
| _Threshold_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies a value between 0 and 10 which defines the maximum threshold for throttling. The Request Manager will remove routing targets if the Health-Score becomes greater than this value.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPThrottlingRulePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Criteria** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementRuleCriteriaPipeBind[]  <br/> ||
|**Expiration** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Threshold** <br/> |Optional  <br/> |System.Nullable  <br/> ||
   
## See also

#### 

[Add-SPThrottlingRule](add-spthrottlingrule.md)
  
[Get-SPThrottlingRule](get-spthrottlingrule.md)
  
[Remove-SPThrottlingRule](remove-spthrottlingrule.md)

