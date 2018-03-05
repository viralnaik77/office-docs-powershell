---
title: "New-SPEnterpriseSearchResultItemType"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45fae4e2-4ca1-4edc-b16a-1b9ea67d16cd

description: "Creates a new result item type."
---

# New-SPEnterpriseSearchResultItemType

Creates a new result item type.
  
```
New-SPEnterpriseSearchResultItemType -DisplayTemplateUrl <String> -Name <String> -Rules <PropertyRuleCollection> <COMMON PARAMETERS>

```

## Example

--------EXAMPLE--------
  
```
$rule = Get-SPEnterpriseSearchPropertyRule -PropertyName "ContentTypeId" -Operator "StartsWith"$rule.AddValue( "0x010063C2F478ACC511DFB869B5BFDFD720851252" 
```

```
$ruleCollection = Get-SPEnterpriseSearchPropertyRuleCollection$ruleCollection.Add( $rule )
```

```
$displayProperties = "WorkId,Rank,Title,Size,Path,Description,SiteName,HitHighlightedSummary,HitHighlightedProperties,ViewsLifeTime"
```

```
$displaytemplateUrl = "~sitecollection/_catalogs/masterpage/Display Templates/Search/Item_MyCustomDisplayTemplate.js"
```

```
$web = Get-SPWeb "UrlOfTheSite"
```

```
$tenantOwner = Get-SPEnterpriseSearchOwner -Level SPSite -SPWeb $web
```

```
$svcAppProxy = Get-SPEnterpriseSearchServiceApplicationProxy
```

```
New-SPEnterpriseSearchResultItemType -SearchApplicationProxy $svcAppProxy `-Name "CustomResultType" `-Rules $ruleCollection `-RulePriority 1 `-DisplayProperties $displayProperties `-DisplayTemplateUrl $displaytemplateUrl `-Owner $tenantOwner
```

This example first defines the rule to apply to the search results in order to target results with a specific property, and adds the rule to the rule collection. Thereafter the example defines the properties of the result that shall be displayed and the URL to the display template governing the appearance of the rendered results. Finally, the example defines the rule item type by its name, the rule collection, the display properties, the display template, and the tenant owner.
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
Use the **New-SPEnterpriseSearchResultItemType** cmdlet to create a new result item type. 
  
Result item types enable you to change the look of search results based on the type of result. You start by defining a collection of rules, which will be evaluated against the properties of results. Then you define the display template to use for rendering that type of result. Once you have created the result item type, results matching the rules of the result item type will render using the specified display template.
  
Example use cases:
  
- Change the look of results for a particular file name extension, for example Word documents.
    
- Change the look of a particular content type in search results.
    
- Change the look of results from a particular author.
    
- Add a result action to results from a particular result source as part of a custom search application.
    
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _DisplayTemplateUrl_ <br/> |Required  <br/> |System.String  <br/> |Specifies the URL of the display template that shall be used for rendering the results. Specify an absolute URL.  <br/> |
| _ExistingResultItemType_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ResultItemTypePipeBind  <br/> |Specifies an existing result item type to which new rules or displayed properties can be added.  <br/> |
| _ExistingResultItemTypeOwner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the search object owner that defines the scope at which an existing result item type was created.  <br/> |
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the result item type.  <br/> |
| _Owner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the search object owner that defines the scope at which the result item type is created.  <br/> |
| _Rules_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.PropertyRuleCollection  <br/> |Specifies the collection of rules to evaluate the result properties against.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DisplayProperties_ <br/> |Optional  <br/> |System.String  <br/> |Specifies which result properties to display.  <br/> |
| _OptimizeForFrequentUse_ <br/> |Optional  <br/> |System.Boolean  <br/> |Enable this flag if you always want the properties of this result item type to be requested, regardless of whether the result type is triggered. This will improve performance as long as it is only enabled on the most frequently used result item types.  <br/> |
| _RulePriority_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies which priority the collection of rules has compared to other rules.  <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the result item type. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _SearchApplicationProxy_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationProxyPipeBind  <br/> |Specifies the proxy of the search application that contains the result item type. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application proxy name (for example, SearchAppProxy1); or an instance of a valid **SearchServiceApplicationProxy** object.  <br/> |
| _SourceID_ <br/> |Optional  <br/> |System.Guid  <br/> |Identifies the search result source that the result item type applies to. Leave this parameter blank to apply to all result sources.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**Rules** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.PropertyRuleCollection  <br/> ||
|**RulePriority** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**DisplayProperties** <br/> |Optional  <br/> |System.String  <br/> ||
|**SourceID** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**DisplayTemplateUrl** <br/> |Required  <br/> |System.String  <br/> ||
|**ExistingResultItemType** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ResultItemTypePipeBind  <br/> ||
|**ExistingResultItemTypeOwner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**Owner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**OptimizeForFrequentUse** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**SearchApplicationProxy** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationProxyPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Set-SPEnterpriseSearchResultItemType](set-spenterprisesearchresultitemtype.md)
  
[Get-SPEnterpriseSearchResultItemType](get-spenterprisesearchresultitemtype.md)
  
[Remove-SPEnterpriseSearchResultItemType](remove-spenterprisesearchresultitemtype.md)
  
[Get-SPEnterpriseSearchOwner](get-spenterprisesearchowner.md)
  
[Get-SPEnterpriseSearchPropertyRule](get-spenterprisesearchpropertyrule.md)
  
[Get-SPEnterpriseSearchPropertyRuleCollection](get-spenterprisesearchpropertyrulecollection.md)

