---
title: "Get-SPEnterpriseSearchMetadataMapping"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 840b9079-bd0d-4574-ab9b-515e8cf7cbf4

description: "Returns the current status of a managed property mapping."
---

# Get-SPEnterpriseSearchMetadataMapping

Returns the current status of a managed property mapping.
  
```
Get-SPEnterpriseSearchMetadataMapping -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-CrawledProperty <CrawledPropertyPipeBind>] [-ManagedProperty <ManagedPropertyPipeBind>] [-SiteCollection <Guid>] [-Tenant <Guid>]

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication
```

```
$mp = Get-SPEnterpriseSearchMetadataManagedProperty -SearchApplication $searchapp -Identity UserName

```

```
Get-SPEnterpriseSearchMetadataMapping -SearchApplication $searchapp -ManagedProperty $mp
```

This example lists all crawled properties mapped to the managed property  `UserName` for the default search service application. 
  
## Detailed Description

This cmdlet reads a **Mapping** object when a managed property mapping is created, updated, or deleted. **SPEnterpriseSearchMetadataMapping** represents a category of a mapping between a managed property and one or more crawled properties in the enterprise search metadata property schema. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the metadata mapping.  <br/> The type must be a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CrawledProperty_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawledPropertyPipeBind  <br/> |Specifies the crawled property from which to return mappings.  <br/> The type must be a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid URL in the form http://server_name, or an instance of a valid **CrawledProperty** object.  <br/> |
| _ManagedProperty_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ManagedPropertyPipeBind  <br/> |Specifies the managed property from which to return mappings.  <br/> The type must be a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid name of a managed property, for example, ManagedProperty1, or an instance of a valid **ManagedProperty** object.  <br/> |
| _SiteCollection_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the metadata mappings returned are to be within the scope of a site collection (SPSite).  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _Tenant_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the metadata mappings returned are to be within the scope of a tenant.  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CrawledProperty** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawledPropertyPipeBind  <br/> ||
|**ManagedProperty** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ManagedPropertyPipeBind  <br/> ||
|**SiteCollection** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**Tenant** <br/> |Optional  <br/> |System.Guid  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchMetadataMapping](new-spenterprisesearchmetadatamapping.md)
  
[Set-SPEnterpriseSearchMetadataMapping](set-spenterprisesearchmetadatamapping.md)
  
[Remove-SPEnterpriseSearchMetadataMapping](remove-spenterprisesearchmetadatamapping.md)

