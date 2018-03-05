---
title: "Get-SPEnterpriseSearchPropertyRule"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 019159bd-d7cd-4321-94bb-285f51ab7bc5

description: "Returns a property rule instance, which can be used in result item types."
---

# Get-SPEnterpriseSearchPropertyRule

Returns a property rule instance, which can be used in result item types.
  
```
Get-SPEnterpriseSearchPropertyRule -Operator <IsEqual | NotEqual | Contains | NotContains | LessThan | GreaterThan | StartsWith> -PropertyName <String> [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

--------EXAMPLE--------
  
```
$rule = Get-SPEnterpriseSearchPropertyRule -PropertyName "ContentTypeId" -Operator "StartsWith"

```

```
$rule.AddValue( "0x010063C2F478ACC511DFB869B5BFDFD720851252" )
```

This example returns a rule for the property "ContentTypeId", where the condition is that the property shall start with a specific value. The second step specifies the value that the property shall start with.
  
## Detailed Description

The **Get-SPEnterpriseSearchPropertyRule** cmdlet returns an instance of a property rule, given the specified condition. The value for the condition is set in a separate step. Such a rule can be used in result item types, to group the results based on the condition of a result property. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Operator_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.PropertyRuleOperator+DefaultOperator  <br/> |Specifies the operation to apply to the property, for example "Starts with".  <br/> |
| _PropertyName_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the property that the rule concerns.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**PropertyName** <br/> |Required  <br/> |System.String  <br/> ||
|**Operator** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.PropertyRuleOperator+DefaultOperator  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchPropertyRuleCollection](get-spenterprisesearchpropertyrulecollection.md)

