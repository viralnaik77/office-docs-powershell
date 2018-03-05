---
title: "Set-SPEnterpriseSearchMetadataMapping"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aff22bea-cb4d-418e-bd54-507958f06580

description: "Sets the properties of a managed property mapping for a search service application."
---

# Set-SPEnterpriseSearchMetadataMapping

Sets the properties of a managed property mapping for a search service application.
  
```
Set-SPEnterpriseSearchMetadataMapping -Identity <MappingPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-CrawledProperty <CrawledPropertyPipeBind>] [-ManagedProperty <ManagedPropertyPipeBind>] [-SearchApplication <SearchServiceApplicationPipeBind>] [-SiteCollection <Guid>] [-Tenant <Guid>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication
```

```
## Get the crawl property to set to, in this case a new property is created
$cat = Get-SPEnterpriseSearchMetadataCategory -SearchApplication $searchapp -Identity People
```

```
$cp = Get-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $searchapp -Category $cat -Limit 1
```

```
$ncp = New-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $searchapp -Name "MyNewCrawlProp" -PropSet $cp.PropSet -Category $cp.CategoryName -IsNameEnum $false -VariantType $cp.VariantType -IsMappedToContents $true
```

```
## Get the mapping to replace
$mycp = Get-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $searchapp -Name MyCrawlProp

```

```
$map = Get-SPEnterpriseSearchMetadataMapping -SearchApplication $searchapp -ManagedProperty $mp -CrawledProperty $mycp
```

```
## Set the new crawl property to map to for this mapping
Set-SPEnterpriseSearchMetadataMapping -Identity $map -SearchApplication $searchapp -CrawledProperty $ncp
```

This example updates an existing mapping between the managed property  `UserName` and the crawled property  `MyCrawlProp` (see [New-SPEnterpriseSearchMetadataMapping](new-spenterprisesearchmetadatamapping.md)) for the default search service application. The crawled property is replaced with a new crawled property named  `MyNewCrawlProp`.
  
## Detailed Description

This cmdlet updates properties of a managed property mapping. **SPEnterpriseSearchMetadataMapping** represents a mapping between a managed property and one or more crawled properties in the enterprise search metadata property schema. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.MappingPipeBind  <br/> |Specifies the metadata mapping to update.  <br/> The type must be a valid URL, in the form http://server_name, or an instance of a valid **Mapping** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _CrawledProperty_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawledPropertyPipeBind  <br/> |Specifies the crawled property to map.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid URL in the form http://server_name, or an instance of a valid **CrawledProperty** object.  <br/> Note: Null indicates that the value is unchanged.  <br/> |
| _ManagedProperty_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ManagedPropertyPipeBind  <br/> |Specifies the managed property to receive the crawled property mapping.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid name of a managed property, for example, ManagedProperty1, or an instance of a valid **ManagedProperty** object.  <br/> Note: Null indicates that the value is unchanged.  <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the metadata mapping.  <br/> The type be a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _SiteCollection_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the metadata mappings returned are to be within the scope of a site collection (SPSite).  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _Tenant_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the metadata mappings returned are to be within the scope of a tenant.  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.MappingPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**CrawledProperty** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawledPropertyPipeBind  <br/> ||
|**ManagedProperty** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ManagedPropertyPipeBind  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**SiteCollection** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**Tenant** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchMetadataMapping](new-spenterprisesearchmetadatamapping.md)
  
[Get-SPEnterpriseSearchMetadataMapping](get-spenterprisesearchmetadatamapping.md)
  
[Remove-SPEnterpriseSearchMetadataMapping](remove-spenterprisesearchmetadatamapping.md)
#### 

[VARIANT Type Constants](https://msdn.microsoft.com/en-us/library/cc237865.aspx)

