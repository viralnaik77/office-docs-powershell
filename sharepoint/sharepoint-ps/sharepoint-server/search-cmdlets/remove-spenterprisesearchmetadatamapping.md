---
title: "Remove-SPEnterpriseSearchMetadataMapping"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6e686288-92ec-447d-ae0d-506816d43119

description: "Deletes a metadata mapping from a managed property."
---

# Remove-SPEnterpriseSearchMetadataMapping

Deletes a metadata mapping from a managed property.
  
```
Remove-SPEnterpriseSearchMetadataMapping -Identity <MappingPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-SearchApplication <SearchServiceApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]

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
$cp = Get-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $searchapp -Category $cat -Limit 1
```

```
$mycp = New-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $searchapp -Name "MyCrawlProp" -PropSet $cp.PropSet -Category $cp.CategoryName -IsNameEnum $false -VariantType $cp.VariantType
```

```
$mp = Get-SPEnterpriseSearchMetadataManagedProperty -SearchApplication $searchapp -Identity UserName
```

```
New-SPEnterpriseSearchMetadataMapping -SearchApplication $searchapp -ManagedProperty $mp -CrawledProperty $mycp
```

```
# Retrieve the new mapping
$map = Get-SPEnterpriseSearchMetadataMapping -SearchApplication $searchapp -ManagedProperty $mp -CrawledProperty $mycp

```

```
Remove-SPEnterpriseSearchMetadataMapping -Identity $map -confirm:$false
```

This example removes an existing mapping between the managed property  `UserName` and the crawled property  `MyCrawlProp` (see [Set-SPEnterpriseSearchMetadataMapping](set-spenterprisesearchmetadatamapping.md)) for the default search service application.
  
## Detailed Description

This cmdlet deletes mappings from a managed property. A metadata mapping is the mapping between a managed property and one or more crawled properties in the enterprise search metadata property schema.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.MappingPipeBind  <br/> |Specifies the metadata mapping to delete.  <br/> The type must be a valid URL, in the form http://server_name, or an instance of a valid **Mapping** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the managed property collection.  <br/> The type must be a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.MappingPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchMetadataMapping](get-spenterprisesearchmetadatamapping.md)
  
[New-SPEnterpriseSearchMetadataMapping](new-spenterprisesearchmetadatamapping.md)
  
[Set-SPEnterpriseSearchMetadataMapping](set-spenterprisesearchmetadatamapping.md)

