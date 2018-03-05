---
title: "Get-SPEnterpriseSearchContentEnrichmentConfiguration"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e34c7111-0b06-47f1-a37e-b6cb36088b6b

description: "Returns the content enrichment configuration for the specified Search service application."
---

# Get-SPEnterpriseSearchContentEnrichmentConfiguration

Returns the content enrichment configuration for the specified Search service application.
  
```
Get-SPEnterpriseSearchContentEnrichmentConfiguration -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

------------------EXAMPLE-----------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication

```

```
Get-SPEnterpriseSearchContentEnrichmentConfiguration -SearchApplication $ssa
```

This example retrieves the **ContentEnrichmentConfiguration** object from the default **SearchServiecApplication**. 
  
## Detailed Description

This cmdlet returns the **ContentEnrichmentConfiguration** object for the **SearchServiceApplication**. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the **SearchServiceApplication** that contains the **ContentEnrichmentConfiguration**.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[Set-SPEnterpriseSearchContentEnrichmentConfiguration](set-spenterprisesearchcontentenrichmentconfiguration.md)
  
[New-SPEnterpriseSearchContentEnrichmentConfiguration](new-spenterprisesearchcontentenrichmentconfiguration.md)
  
[Remove-SPEnterpriseSearchContentEnrichmentConfiguration](remove-spenterprisesearchcontentenrichmentconfiguration.md)
  
[Get-SPEnterpriseSearchServiceApplication](get-spenterprisesearchserviceapplication.md)

