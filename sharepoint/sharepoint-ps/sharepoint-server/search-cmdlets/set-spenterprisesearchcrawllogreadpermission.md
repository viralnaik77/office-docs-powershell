---
title: "Set-SPEnterpriseSearchCrawlLogReadPermission"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ff291003-4189-497e-9236-16c8333a4075

description: "Grants users permission to view the crawl log information."
---

# Set-SPEnterpriseSearchCrawlLogReadPermission

Grants users permission to view the crawl log information.
  
```
Set-SPEnterpriseSearchCrawlLogReadPermission [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Identity <CrawlLogReadPermissionPipeBind>] [-SearchApplication <SearchServiceApplicationPipeBind>] [-Tenant <Guid>] [-UserNames <String>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------EXAMPLE --------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
```

```
$crawlLogPermission = Get-SPEnterpriseSearchCrawlLogReadPermission -SearchApplication $ssa -Tenant "00000000-0000-0000-0000-000000000001"
```

```
Set-SPEnterpriseSearchCrawlLogReadPermission -Identity $crawlLogPermission -SearchApplication $ssa -UserNames "user1;user2" -Tenant "00000000-0000-0000-0000-000000000001"

```

This example first defines **$crawlLogPermission**, which is the list of users who have permission to view the crawl log information from the tenant with id "00000000-0000-0000-0000-000000000001" on the search application referenced by **$ssa**. Then the example uses the **Set-SPEnterpriseSearchCrawlLogReadPermission** cmdlet to add user1 and user2 to the list of users referenced by **$crawlLogPermission**. 
  
## Detailed Description

Only the Search Service Application administrator can use this cmdlet. 
  
The administrator uses the **Set-SPEnterpriseSearchCrawlLogReadPermission** cmdlet to grant users permission to view crawl log information. The administrator can choose to restrict the permission to crawl log information from a particular tenant. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawlLogReadPermissionPipeBind  <br/> |Specifies the crawl log permissions list to which users should be added.  <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the crawl log. The type must be a valid GUID, of the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _Tenant_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the users shall be added to the crawl log permissions list within the scope of this tenant only. The type must be a valid GUID of the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _UserNames_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the user names that shall be granted permission to view the crawl log information Use "domain\username" or "username". When adding several user names, separate names with semi-colons.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawlLogReadPermissionPipeBind  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**Tenant** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**UserNames** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchCrawlLogReadPermission](get-spenterprisesearchcrawllogreadpermission.md)
  
[Remove-SPEnterpriseSearchCrawlLogReadPermission](remove-spenterprisesearchcrawllogreadpermission.md)

