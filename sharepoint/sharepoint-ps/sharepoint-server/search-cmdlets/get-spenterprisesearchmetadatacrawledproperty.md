---
title: "Get-SPEnterpriseSearchMetadataCrawledProperty"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0aff3f02-ef56-4ac3-8a32-254f3d6365e3

description: "Returns a crawled property."
---

# Get-SPEnterpriseSearchMetadataCrawledProperty

Returns a crawled property.
  
```
Get-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Category <CategoryPipeBind>] [-Limit <String>] [-Name <String>] [-PropSet <Guid>] [-SiteCollection <Guid>] [-Tenant <Guid>] [-VariantType <Int32>]

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication
```

```
$cat = Get-SPEnterpriseSearchMetadataCategory -SearchApplication $searchapp -Identity People

```

```
Get-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $searchapp -Category $cat -Limit 1
```

This example returns the first crawled property in the  `PeopleSearch_Scope` metadata category for the default search service application. 
  
## Detailed Description

This cmdlet reads a **CrawledProperty** object for a crawled property that was created or updated. You should run this cmdlet when the search functionality is configured for the first time, and after new crawled properties are discovered during a crawl. If the **Name** parameter is not specified, this cmdlet returns all crawled properties for the specified category for the specified search application. If neither the **Name** nor the **Category** parameter is specified, this cmdlet returns all crawled properties for the specified search application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the crawled property.  <br/> The type must be a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Category_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CategoryPipeBind  <br/> |Specifies the metadata category of the crawled property to return.  <br/> The type must be a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid name of a metadata category, for example, MetadataCategory1, or an instance of a valid **Category** object.  <br/> |
| _Limit_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the maximum number of items to return. Specify **ALL** to return all possible results.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the crawled property to retrieve.  <br/> The type must be a valid crawled property name, for example "urn:schemas-microsoft-com:sharepoint:portal:profile:UserName"  <br/> |
| _PropSet_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies to return crawled properties that use the specified property set. A property set belongs to one crawled property category.  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _SiteCollection_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the crawled properties returned are to be within the scope of a site collection (SPSite).  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _Tenant_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the crawled properties returned are to be within the scope of a tenant.  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _VariantType_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies to return crawled properties that use the specified variant type.  <br/> The type must be an integer that specifies the variant data type of the property set.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Category** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CategoryPipeBind  <br/> ||
|**Limit** <br/> |Optional  <br/> |System.String  <br/> ||
|**PropSet** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**SiteCollection** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**Tenant** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**VariantType** <br/> |Optional  <br/> |System.Nullable  <br/> ||
   

