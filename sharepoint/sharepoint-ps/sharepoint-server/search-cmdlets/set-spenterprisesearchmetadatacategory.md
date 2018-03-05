---
title: "Set-SPEnterpriseSearchMetadataCategory"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cd69f7af-dabe-4a09-88a9-b0bcbba2fa9e

description: "Sets properties of a crawled property category."
---

# Set-SPEnterpriseSearchMetadataCategory

Sets properties of a crawled property category.
  
```
Set-SPEnterpriseSearchMetadataCategory -Identity <CategoryPipeBind> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-AutoCreateNewManagedProperties <$true | $false>] [-Confirm [<SwitchParameter>]] [-DiscoverNewProperties <$true | $false>] [-MapToContents <$true | $false>] [-Name <String>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication
```

```
Set-SPEnterpriseSearchMetadataCategory -Identity People -SearchApplication $searchapp -DiscoverNewProperties $false -MapToContents $false
```

This example sets both  `DiscoverNewProperties` and  `MapToContents` properties to  `False` for the  `People` category for the default search service application. 
  
## Detailed Description

This cmdlet updates properties of a crawled property category when the search functionality is configured for the first time, and after a new crawled property category is discovered during a crawl. **SPEnterpriseSearchMetadataCategory** represents a category in the enterprise search metadata property schema. 
  
Note that a category may represent multiple propsets. Changes to the category will overwrite all propsets.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.CategoryPipeBind  <br/> |Specifies the metadata category to update.  <br/> The type must be a valid name of a metadata category, for example, MetadataCategory1, or an instance of a valid **Category** object.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the enterprise search metadata categories.  <br/> The type must be a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _AutoCreateNewManagedProperties_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that when a new crawled property in this category is found, a corresponding managed property is created and mapped to this new crawled property.  <br/> Note:Null indicates that the value is unchanged.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DiscoverNewProperties_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that if there are unknown properties in this category, these new properties are discovered during a crawl.  <br/> Note:Null indicates that the value is unchanged.  <br/> |
| _MapToContents_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that all crawled properties of type string are mapped to corresponding managed properties of this category.  <br/> Note:Null indicates that the value is unchanged.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the enterprise search metadata category.  <br/> The type must be a valid name of a metadata category, for example MetadataCategory1.  <br/> Note:Null indicates that the value is unchanged.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.CategoryPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**AutoCreateNewManagedProperties** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DiscoverNewProperties** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MapToContents** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchMetadataCategory](new-spenterprisesearchmetadatacategory.md)
  
[Get-SPEnterpriseSearchMetadataCategory](get-spenterprisesearchmetadatacategory.md)
  
[Remove-SPEnterpriseSearchMetadataCategory](remove-spenterprisesearchmetadatacategory.md)

