---
title: "New-SPRequestManagementRuleCriteria"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1bd148a8-e45d-4ab6-be5e-3e20f3d7fbf4

description: "Creates criteria for the rule to match."
---

# New-SPRequestManagementRuleCriteria

Creates criteria for the rule to match.
  
```
New-SPRequestManagementRuleCriteria -CustomHeader <String> -Value <String> [-CaseSensitive <SwitchParameter>] [-MatchType <Equals | Regex | StartsWith | EndsWith>] <COMMON PARAMETERS>

```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
Use the **New-SPRequestManagementRuleCriteria** cmdlet to create criteria for the rule to match. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _CustomHeader_ <br/> |Required  <br/> |System.String  <br/> |Specifies the custom header for the rule.  <br/> |
| _Property_ <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPRequestManagementRulePropertyType  <br/> |Specifies a header for a value to match.  <br/> The following are the valid values:  <br/> --Url  <br/> --Urlreferrer  <br/> --UserAgent  <br/> --Host  <br/> --IP  <br/> --HttpMethod  <br/> --SoapAction  <br/> --CustomHeader  <br/> |
| _Value_ <br/> |Required  <br/> |System.String  <br/> |Specifies a value for the rule to match.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CaseSensitive_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether or not the match is case sensitive.  <br/> |
| _MatchType_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPRequestManagementRuleMatchType  <br/> |Defines operators for the match.  <br/> The following are the valid values:  <br/> --Equals  <br/> --Regex  <br/> --StartsWith  <br/> --EndsWith  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Value** <br/> |Required  <br/> |System.String  <br/> ||
|**CustomHeader** <br/> |Required  <br/> |System.String  <br/> ||
|**Property** <br/> |Required  <br/> |System.Nullable  <br/> ||
|**CaseSensitive** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MatchType** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[Get-SPRequestManagementSettings](get-sprequestmanagementsettings.md)
  
[Set-SPRequestManagementSettings](set-sprequestmanagementsettings.md)

