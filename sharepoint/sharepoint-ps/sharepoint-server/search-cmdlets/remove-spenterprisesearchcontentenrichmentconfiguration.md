---
title: "Remove-SPEnterpriseSearchContentEnrichmentConfiguration"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c45dee4c-1754-4b2b-b5e5-a92b15839f7f

description: "Removes the current content enrichment configuration from the Search service application."
---

# Remove-SPEnterpriseSearchContentEnrichmentConfiguration

Removes the current content enrichment configuration from the Search service application.
  
```
Remove-SPEnterpriseSearchContentEnrichmentConfiguration -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

------------------EXAMPLE-----------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication

```

```
Remove-SPEnterpriseSearchContentEnrichmentConfiguration -SearchApplication $ssa
```

This example removes the content enrichment configuration from the default Search service application.
  
## Detailed Description

This cmdlet removes the current content enrichment configuration from the SearchServiceApplication.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the **SearchServiceApplication** that contains content enrichment configuration.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchContentEnrichmentConfiguration](get-spenterprisesearchcontentenrichmentconfiguration.md)
  
[Set-SPEnterpriseSearchContentEnrichmentConfiguration](set-spenterprisesearchcontentenrichmentconfiguration.md)
  
[New-SPEnterpriseSearchContentEnrichmentConfiguration](new-spenterprisesearchcontentenrichmentconfiguration.md)
  
[Get-SPEnterpriseSearchServiceApplication](get-spenterprisesearchserviceapplication.md)

