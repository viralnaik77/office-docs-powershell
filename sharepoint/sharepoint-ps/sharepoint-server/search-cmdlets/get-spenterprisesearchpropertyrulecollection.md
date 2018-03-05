---
title: "Get-SPEnterpriseSearchPropertyRuleCollection"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7b2a7a2-0f84-4401-8377-663fe44875de

description: "Returns the collection of rules that are applied to search results."
---

# Get-SPEnterpriseSearchPropertyRuleCollection

Returns the collection of rules that are applied to search results.
  
```
Get-SPEnterpriseSearchPropertyRuleCollection [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

--------EXAMPLE--------
  
```
$rule = Get-SPEnterpriseSearchPropertyRule -PropertyName "ContentTypeId" -Operator "StartsWith"$rule.AddValue( "0x010063C2F478ACC511DFB869B5BFDFD720851252" )
```

```
$ruleCollection = Get-SPEnterpriseSearchPropertyRuleCollection
```

```
$ruleCollection.Add( $rule )
```

This example returns a rule for the result property "ContentTypeId", the rule specifies that this property must start with the value "0x010063C2F478ACC511DFB869B5BFDFD720851252". Thereafter the example returns the rule collection, and adds the rule to the rule collection.
  
## Detailed Description

The **Get-SPEnterpriseSearchPropertyRuleCollection** cmdlet returns the collection of rules that are applied to search results. Rules can be added and removed from the rule collection. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchPropertyRule](get-spenterprisesearchpropertyrule.md)

