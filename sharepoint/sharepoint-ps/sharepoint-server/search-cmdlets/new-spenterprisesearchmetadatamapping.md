---
title: "New-SPEnterpriseSearchMetadataMapping"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9d6a7ce8-78df-4c04-91f2-5c2f4e0296c1

description: "Adds a managed property mapping."
---

# New-SPEnterpriseSearchMetadataMapping

Adds a managed property mapping.
  
```
New-SPEnterpriseSearchMetadataMapping -CrawledProperty <CrawledPropertyPipeBind> -ManagedProperty <ManagedPropertyPipeBind> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-SiteCollection <Guid>] [-Tenant <Guid>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet maps a crawled property to a managed property. **SPEnterpriseSearchMetadataMapping** represents a snapshot of a mapping between a managed property and one or more crawled properties in the enterprise search metadata property schema. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**CrawledProperty** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawledPropertyPipeBind  <br/> |Specifies the crawled property to map.  <br/> The type must be a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid URL in the form http://server_name, or an instance of a valid **CrawledProperty** object.  <br/> |
|**ManagedProperty** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ManagedPropertyPipeBind  <br/> |Specifies the managed property to which the crawled property should be mapped.  <br/> The type must be a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid name of a managed property, for example, ManagedProperty1, or an instance of a valid **ManagedProperty** object.  <br/> |
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the metadata mapping.  <br/> The type must be a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**SiteCollection** <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the metadata mapping returned are to be within the scope of a site collection (SPSite).  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
|**Tenant** <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the metadata mapping returned are to be within the scope of a tenant.  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**CrawledProperty** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawledPropertyPipeBind  <br/> ||
|**ManagedProperty** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ManagedPropertyPipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SiteCollection** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**Tenant** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication
```

```
$mp = Get-SPEnterpriseSearchMetadataManagedProperty -SearchApplication $searchapp -Identity UserName
```

```
$cat = Get-SPEnterpriseSearchMetadataCategory -SearchApplication $searchapp -Identity People
```

```
$cp = Get-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $searchapp -Category $cat -Limit 1
```

```
$ncp = New-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $searchapp -Name "MyCrawlProp" -PropSet $cp.PropSet -Category $cp.CategoryName -IsNameEnum $false -VariantType $cp.VariantType -IsMappedToContents $true

```

```
New-SPEnterpriseSearchMetadataMapping -SearchApplication $searchapp -ManagedProperty $mp -CrawledProperty $ncp
```

This example maps the created crawled property  `MyCrawlProp` to the managed property  `UserName` for the default search service application. 
  
## See also

#### 

[Get-SPEnterpriseSearchMetadataMapping](get-spenterprisesearchmetadatamapping.md)
  
[Set-SPEnterpriseSearchMetadataMapping](set-spenterprisesearchmetadatamapping.md)
  
[Remove-SPEnterpriseSearchMetadataMapping](remove-spenterprisesearchmetadatamapping.md)
#### 

[VARIANT Type Constants (http://go.microsoft.com/fwlink/p/?LinkId=143322&amp;clcid=0x409)](http://go.microsoft.com/fwlink/p/?LinkId=143322&amp;clcid=0x409)

