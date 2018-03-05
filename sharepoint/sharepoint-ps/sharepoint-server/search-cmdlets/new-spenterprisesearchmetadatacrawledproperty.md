---
title: "New-SPEnterpriseSearchMetadataCrawledProperty"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3015484-e301-48b1-88ba-4f3a01bf13e4

description: "Adds a crawled property."
---

# New-SPEnterpriseSearchMetadataCrawledProperty

Adds a crawled property.
  
```
New-SPEnterpriseSearchMetadataCrawledProperty -Category <CategoryPipeBind> -IsNameEnum <$true | $false> -Name <String> -PropSet <Guid> -SearchApplication <SearchServiceApplicationPipeBind> -VariantType <Int32> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-IsMappedToContents <$true | $false>] [-SiteCollection <Guid>] [-Tenant <Guid>] [-WhatIf [<SwitchParameter>]]

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
$crawlprop = Get-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $searchapp -Category $cat -Limit 1

```

```
New-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $searchapp -Name "MyCrawlProp" -PropSet $crawlprop.PropSet -Category $crawlprop.CategoryName -IsNameEnum $false -VariantType $crawlprop.VariantType -IsMappedToContents $false
```

This example maps the new crawled property  `MyCrawlProp` to the  `People` metadata category for the default search service application. The mapping uses the constraints from the existing  `People` category. 
  
## Detailed Description

This cmdlet is used when the search functionality is configured for the first time, and to add new crawled properties after the first configuration. **SPEnterpriseSearchMetadataCrawledProperty** represents a crawled property in the enterprise search metadata property schema. Or, crawled properties are automatically created during regular crawls (see SPEnterpriseSearchMetadataCategory). 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Category_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.CategoryPipeBind  <br/> |Specifies to which metadata category the crawled property should be added  <br/> The type must be a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid name of a metadata category, for example, MetadataCategory1, or an instance of a valid **Category** object.  <br/> |
| _IsNameEnum_ <br/> |Required  <br/> |System.Boolean  <br/> |Specifies whether the crawled property name is of type integer. Specified by true or false.  <br/> |
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the identity of the new crawled property.  <br/> The type must be a valid crawled property name, for example "urn:schemas-microsoft-com:sharepoint:portal:profile:UserName"  <br/> |
| _PropSet_ <br/> |Required  <br/> |System.Guid  <br/> |Specifies the property set that belongs to an existing category.  <br/> A valid GUID that specifies the property set, in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the crawled property.  <br/> The type must be a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _VariantType_ <br/> |Required  <br/> |System.Int32  <br/> |Adds the crawled property as the specified variant type. For more information about valid values for this property, see [VARIANT Type Constants](http://go.microsoft.com/fwlink/p/?LinkId=143322&amp;clcid=0x409) (http://go.microsoft.com/fwlink/p/?LinkId=143322&amp;clcid=0x409).  <br/> The type must be an integer that specifies the variant data type of the property set.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _IsMappedToContents_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that the crawled property should be mapped to managed properties. Specify **true** to map a crawled property to a managed property.  <br/> |
| _SiteCollection_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the crawled properties returned are to be within the scope of a site collection (SPSite).  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _Tenant_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the crawled properties returned are to be within the scope of a tenant.  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Category** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.CategoryPipeBind  <br/> ||
|**IsNameEnum** <br/> |Required  <br/> |System.Boolean  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**PropSet** <br/> |Required  <br/> |System.Guid  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**VariantType** <br/> |Required  <br/> |System.Int32  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**IsMappedToContents** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**SiteCollection** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**Tenant** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchMetadataCrawledProperty](get-spenterprisesearchmetadatacrawledproperty.md)
  
[Set-SPEnterpriseSearchMetadataCrawledProperty](set-spenterprisesearchmetadatacrawledproperty.md)
#### 

[VARIANT Type Constants (http://go.microsoft.com/fwlink/p/?LinkId=143322&amp;clcid=0x409)](http://go.microsoft.com/fwlink/p/?LinkId=143322&amp;clcid=0x409)

