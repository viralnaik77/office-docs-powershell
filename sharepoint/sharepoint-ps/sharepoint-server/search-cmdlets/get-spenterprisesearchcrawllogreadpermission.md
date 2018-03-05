---
title: "Get-SPEnterpriseSearchCrawlLogReadPermission"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6a9f8f69-8d56-43b2-80b1-fcd6999acc27

description: "Retrieves the list of users with permission to access the crawl log information."
---

# Get-SPEnterpriseSearchCrawlLogReadPermission

Retrieves the list of users with permission to access the crawl log information.
  
```
Get-SPEnterpriseSearchCrawlLogReadPermission -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Tenant <Guid>]

```

## Example

--------EXAMPLE--------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication

```

```
Get-SPEnterpriseSearchCrawlLogReadPermission -SearchApplication $ssa -Tenant "00000000-0000-0000-0000-000000000001"
```

This example retrieves a list of users who have permission to view the crawl log information for a tenant with id "00000000-0000-0000-0000-000000000001" on the search application referenced by **$ssa**. 
  
## Detailed Description

Only the Search Service Application administrator can use the **Get-SPEnterpriseSearchCrawlLogReadPermission** cmdlet. 
  
The Search Service Application administrator uses the cmdlet to retrieve a list of users with permission to view the crawl log information. The administrator can choose to limit this list to users with permission to view crawl log information from a particular tenant.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the name of the search application for which to list crawl log permissions. The type must be a valid GUID, of the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Tenant_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the list of users shall be within the scope of this tenant. The type must be a valid GUID of the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Tenant** <br/> |Optional  <br/> |System.Guid  <br/> ||
   
## See also

#### 

[Set-SPEnterpriseSearchCrawlLogReadPermission](set-spenterprisesearchcrawllogreadpermission.md)
  
[Remove-SPEnterpriseSearchCrawlLogReadPermission](remove-spenterprisesearchcrawllogreadpermission.md)

