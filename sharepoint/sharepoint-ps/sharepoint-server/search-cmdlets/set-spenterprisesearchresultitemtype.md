---
title: "Set-SPEnterpriseSearchResultItemType"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d67c8e9-2ebc-4a36-b6ea-460adf6fa15d

description: "Sets properties of a result item type."
---

# Set-SPEnterpriseSearchResultItemType

Sets properties of a result item type.
  
```
Set-SPEnterpriseSearchResultItemType -Identity <ResultItemTypePipeBind> -Owner <SearchObjectOwner> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DisplayProperties <String>] [-DisplayTemplateUrl <String>] [-Name <String>] [-OptimizeForFrequentUse <$true | $false>] [-RulePriority <Int32>] [-Rules <PropertyRuleCollection>] [-SearchApplication <SearchServiceApplicationPipeBind>] [-SearchApplicationProxy <SearchServiceApplicationProxyPipeBind>] [-SourceID <Guid>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------EXAMPLE--------
  
```
$web = Get-SPWeb "UrlOfTheSite"
```

```
$tenantOwner = Get-SPEnterpriseSearchOwner -Level SPSite -SPWeb $web
```

```
$searchapp = Get-SPEnterpriseSearchServiceApplication
```

```
$resultType = Get-SPEnterpriseSearchResultItemType -Owner $tenantOwner -SearchApplication $searchapp
```

```
$resultType.BuiltIn
```

```
$rule = Get-SPEnterpriseSearchPropertyRule -PropertyName "ContentTypeId" -Operator "StartsWith"$rule.AddValue( "0x010063C2F478ACC511DFB869B5BFDFD720851252" )
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
Set-SPEnterpriseSearchResultItemType -Identity $resultType `-SearchApplication $searchapp `-Name "CustomResultType" `-Rules $ruleCollection `-RulePriority 1 `-DisplayProperties $displayProperties `-DisplayTemplateUrl $displaytemplateUrl `-Owner $tenantOwner
```

This example first defines variables for the URL of the site, the search owner, and search application. It retrieves the result item type and checks whether the result item type is a built-in result item type. If  `$resultType.BuiltIn` returns false then the result item type is not built-in and you can set its properties by using the **Set-SPEnterpriseSearchResultItemType**. 
  
Next, the example creates the rule that result item types shall be matched against, and adds it to a property rule collection. 
  
Next, the example defines which properties of the result item type that shall be displayed and the display template to use.
  
Finally, the example uses the **Set-SPEnterpriseSearchResultItemType** cmdlet to modify the result item type. 
  
## Detailed Description

The **Set-SPEnterpriseSearchResultItemType** cmdlet sets properties of user-created result item types. You cannot use this cmdlet to set or change properties of the built-in result item types that are included with SharePoint products. 
  
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
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ResultItemTypePipeBind  <br/> |Specifies the result item type to update. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _Owner_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the search object owner that defines the scope at which the result item type was created.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DisplayProperties_ <br/> |Optional  <br/> |System.String  <br/> |Specifies which result properties to display.  <br/> |
| _DisplayTemplateUrl_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the URL of the display template that shall be used for rendering the results.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the result item type.  <br/> |
| _OptimizeForFrequentUse_ <br/> |Optional  <br/> |System.Boolean  <br/> |Enable this flag if you always want the properties of this result item type to be requested, regardless of whether the result type is triggered. This will improve performance as long as it is only enabled on the most frequently used result item types.  <br/> |
| _RulePriority_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies which priority the collection of rules has compared to other rules.  <br/> |
| _Rules_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.PropertyRuleCollection  <br/> |Specifies the collection of rules to evaluate the result properties against.  <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the name of the search application. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _SearchApplicationProxy_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationProxyPipeBind  <br/> |Specifies the proxy of the search application that contains the result item type. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application proxy name (for example, SearchAppProxy1); or an instance of a valid **SearchServiceApplicationProxy** object.  <br/> |
| _SourceID_ <br/> |Optional  <br/> |System.Guid  <br/> |A valid GUID that identifies the search result source that the result item type applies to.  <br/> The GUID should be in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ResultItemTypePipeBind  <br/> ||
|**Owner** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DisplayProperties** <br/> |Optional  <br/> |System.String  <br/> ||
|**DisplayTemplateUrl** <br/> |Optional  <br/> |System.String  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**OptimizeForFrequentUse** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**RulePriority** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Rules** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.PropertyRuleCollection  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**SearchApplicationProxy** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationProxyPipeBind  <br/> ||
|**SourceID** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchResultItemType](new-spenterprisesearchresultitemtype.md)
  
[Get-SPEnterpriseSearchResultItemType](get-spenterprisesearchresultitemtype.md)
  
[Remove-SPEnterpriseSearchResultItemType](remove-spenterprisesearchresultitemtype.md)
  
[Get-SPEnterpriseSearchOwner](get-spenterprisesearchowner.md)
  
[Get-SPEnterpriseSearchPropertyRule](get-spenterprisesearchpropertyrule.md)
  
[Get-SPEnterpriseSearchPropertyRuleCollection](get-spenterprisesearchpropertyrulecollection.md)

