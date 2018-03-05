---
title: "New-SPEnterpriseSearchMetadataCategory"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86994e75-e13f-49a9-8147-42b3729ea328

description: "Adds a crawled property category to a search service application."
---

# New-SPEnterpriseSearchMetadataCategory

Adds a crawled property category to a search service application.
  
```
New-SPEnterpriseSearchMetadataCategory -Name <String> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-AutoCreateNewManagedProperties <$true | $false>] [-Confirm [<SwitchParameter>]] [-DiscoverNewProperties <$true | $false>] [-MapToContents <$true | $false>] [-PropSet <Guid>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication
```

```
$guid = [System.Guid]::NewGuid()

```

```
New-SPEnterpriseSearchMetadataCategory -SearchApplication $searchapp -Name MyCategory -DiscoverNewProperties $true -PropSet $guid
```

This example adds a new metadata category named  `MyCategory` to the default search service application. The  `DiscoverNewProperties` parameter is set to  `true`. Therefore, new crawled properties will be added to the  `MyCategory` metadata category and the unique category identifier is set with the  `PropSet` parameter. 
  
## Detailed Description

This cmdlet creates the new crawled property category. **SPEnterpriseSearchMetadataCategory** represents a category in the enterprise search metadata property schema. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the identity of the new metadata category.  <br/> The type must be a valid name of a metadata category, for example, MetadataCategory1.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search service application that contains the enterprise search metadata categories.  <br/> The type must be a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _AutoCreateNewManagedProperties_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that when a new crawled property in this category is found, a corresponding managed property is created and mapped to this new crawled property.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DiscoverNewProperties_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that if there are unknown properties in this category, these new properties are discovered during a crawl.  <br/> |
| _MapToContents_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that all crawled properties of type string are mapped to corresponding managed properties of this category.  <br/> |
| _PropSet_ <br/> |Optional  <br/> |System.Guid  <br/> |Creates a new metadata category with the specified property set.  <br/> Note that the specified property set is the identifier of the category. Therefore, two categories cannot share a property set.  <br/> The type must be a valid GUID that specifies the property set, in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**AutoCreateNewManagedProperties** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DiscoverNewProperties** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MapToContents** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**PropSet** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchMetadataCategory](get-spenterprisesearchmetadatacategory.md)
  
[Set-SPEnterpriseSearchMetadataCategory](set-spenterprisesearchmetadatacategory.md)
  
[Remove-SPEnterpriseSearchMetadataCategory](remove-spenterprisesearchmetadatacategory.md)

