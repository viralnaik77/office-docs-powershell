---
title: "Get-SPEnterpriseSearchMetadataManagedProperty"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 048a6d51-71f3-4d47-be19-6fd440f73557

description: "Returns a managed property."
---

# Get-SPEnterpriseSearchMetadataManagedProperty

Returns a managed property.
  
```
Get-SPEnterpriseSearchMetadataManagedProperty -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <ManagedPropertyPipeBind>] [-Limit <String>] [-SiteCollection <Guid>] [-Tenant <Guid>]

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication
```

```
Get-SPEnterpriseSearchMetadataManagedProperty -SearchApplication $searchapp -Identity UserName
```

This example retrieves the managed property  `UserName` from the default search service application. 
  
## Detailed Description

This cmdlet reads a **ManagedProperty** object for managed properties that are created or updated. 
  
If the **Identity** parameter is not specified, this cmdlet returns the managed property collection for the specified search application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the managed property collection.  <br/> The type must be a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ManagedPropertyPipeBind  <br/> |Specifies the managed property to retrieve.  <br/> The type must be a valid name of metadata property, for example MetadataProperty1, or an instance of a valid **ManagedProperty** object.  <br/> |
| _Limit_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the maximum number of managed properties to return. Specify **ALL** to return all possible results.  <br/> |
| _SiteCollection_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the managed properties returned are to be within the scope of a site collection (SPSite).  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _Tenant_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the managed properties returned are to be within the scope of a tenant.  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.ManagedPropertyPipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Limit** <br/> |Optional  <br/> |System.String  <br/> ||
|**SiteCollection** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**Tenant** <br/> |Optional  <br/> |System.Guid  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchMetadataManagedProperty](new-spenterprisesearchmetadatamanagedproperty.md)
  
[Set-SPEnterpriseSearchMetadataManagedProperty](set-spenterprisesearchmetadatamanagedproperty.md)
  
[Remove-SPEnterpriseSearchMetadataManagedProperty](remove-spenterprisesearchmetadatamanagedproperty.md)

