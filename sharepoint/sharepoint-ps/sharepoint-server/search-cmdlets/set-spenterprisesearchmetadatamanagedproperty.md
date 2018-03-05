---
title: "Set-SPEnterpriseSearchMetadataManagedProperty"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 2/11/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f4af923-59c4-47fb-a34e-74370b67e94f

description: "Sets the properties of a metadata managed property."
---

# Set-SPEnterpriseSearchMetadataManagedProperty

Sets the properties of a metadata managed property.
  
```
Set-SPEnterpriseSearchMetadataManagedProperty -Identity <ManagedPropertyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DefaultForQueryIndependentRank <UInt32>] [-Description <String>] [-EnabledForQueryIndependentRank <$true | $false>] [-EnabledForScoping <$true | $false>] [-FullTextQueriable <$true | $false>] [-IncludeInAlertSignature <$true | $false>] [-IncludeInMd5 <$true | $false>] [-Name <String>] [-NameNormalized <$true | $false>] [-NoWordBreaker <$true | $false>] [-RemoveDuplicates <$true | $false>] [-RespectPriority <$true | $false>] [-Retrievable <$true | $false>] [-SafeForAnonymous <$true | $false>] [-SearchApplication <SearchServiceApplicationPipeBind>] [-SiteCollection <Guid>] [-Tenant <Guid>] [-UserFlags <Int16>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication
Set-SPEnterpriseSearchMetadataManagedProperty -SearchApplication $searchapp -Identity UserName -EnabledForScoping $true
```

This example sets the  `EnabledForScoping` property to true for the managed property named  `UserName` in the default search service application. 
  
## Detailed Description

This cmdlet updates the properties of a managed property. It is typically used to change the name or description of a managed property. **SPEnterpriseSearchMetadataManagedProperty** represents a managed property in the enterprise search metadata property schema. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ManagedPropertyPipeBind  <br/> |Specifies the managed property to update.  <br/> The type must be a valid name of a managed property, for example, ManagedProperty1, or an instance of a valid **ManagedProperty** object  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DefaultForQueryIndependentRank_ <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies that the managed property is mandatory when it is used in query-independent rank (relevance).  <br/> Note:Null indicates that the value is unchanged.  <br/> |
| _Description_ <br/> |Optional  <br/> |System.String  <br/> |Adds a description to the metadata managed property.  <br/> The type must be a valid string.  <br/> Note: Null indicates that the value is unchanged.  <br/> |
| _EnabledForQueryIndependentRank_ <br/> |Optional  <br/> |System.Boolean  <br/> | Specifies that the managed property is mandatory when it is used in the custom ranking model for the query-independent work of ranking.  <br/>  The type must be one of the following query-independent ranking features in the custom model XML:  <br/> **queryIndependentFeature** <br/> **categoryFeature** <br/> **languageFeature** <br/>  Note: Null indicates that the value is unchanged.  <br/> |
| _EnabledForScoping_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that the managed property can be used in a scope definition.  <br/> Note: Null indicates that the value is unchanged.  <br/> |
| _FullTextQueriable_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that the managed property can be used in enterprise search SQL queries.  <br/> Note: Null indicates that the value is unchanged.  <br/> |
| _IncludeInAlertSignature_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether this managed property should be included in alert signature.  <br/> |
| _IncludeInMd5_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that the managed property is included in the hash used by the crawler to determine whether a document has changed.  <br/> Note: Null indicates that the value is unchanged.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies a name for the managed property.  <br/> The type must be a valid managed property name, for example ManagedProperty1.  <br/> Note: Null indicates that the value is unchanged.  <br/> |
| _NameNormalized_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies if the values of the managed property should be normalized, that is, enable to return results independent of letter casing and diacritics used in the query. If value is set to **true**, the values are normalized.  <br/> Note: Null indicates that the value is unchanged.  <br/> |
| _NoWordBreaker_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that the values for this managed property are processed by a word breaker.  <br/> Note: Null indicates that the value is unchanged.  <br/> |
| _RemoveDuplicates_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that duplicate values for the managed property are removed.  <br/> |
| _RespectPriority_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that when a mapped crawled property contains multiple values, and **RespectPriority** is set to ** true **, only the first mapped crawled property is copied. Otherwise, all mapped crawled properties that have a value are copied.  <br/> Note: Null indicates that the value is unchanged.  <br/> |
| _Retrievable_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether the values for this managed property are retrievable or not.  <br/> Note: Null indicates that the value is unchanged.  <br/> |
| _SafeForAnonymous_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether it is acceptable to display the contents of the property in search results for anonymous searches.  <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the managed property collection.  <br/> The type must be a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _SiteCollection_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the managed properties returned are to be within the scope of a site collection (SPSite).  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _Tenant_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the managed properties returned are to be within the scope of a tenant.  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _UserFlags_ <br/> |Optional  <br/> |System.Int16  <br/> |Reserved for future use.  <br/> Note: Null indicates that the value is unchanged.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ManagedPropertyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultForQueryIndependentRank** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Description** <br/> |Optional  <br/> |System.String  <br/> ||
|**EnabledForQueryIndependentRank** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**EnabledForScoping** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**FullTextQueriable** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**IncludeInAlertSignature** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**IncludeInMd5** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**NameNormalized** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**NoWordBreaker** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**RemoveDuplicates** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**RespectPriority** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Retrievable** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**SafeForAnonymous** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**SiteCollection** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**Tenant** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**UserFlags** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchMetadataManagedProperty](new-spenterprisesearchmetadatamanagedproperty.md)
  
[Get-SPEnterpriseSearchMetadataManagedProperty](get-spenterprisesearchmetadatamanagedproperty.md)
  
[Remove-SPEnterpriseSearchMetadataManagedProperty](remove-spenterprisesearchmetadatamanagedproperty.md)

