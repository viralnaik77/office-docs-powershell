---
title: "Remove-SPEnterpriseSearchCrawlLogReadPermission"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 23f4c5a2-6102-4b15-a387-67c8af10a249

description: "Removes permission to view crawl log information."
---

# Remove-SPEnterpriseSearchCrawlLogReadPermission

Removes permission to view crawl log information.
  
```
Remove-SPEnterpriseSearchCrawlLogReadPermission [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Identity <CrawlLogReadPermissionPipeBind>] [-SearchApplication <SearchServiceApplicationPipeBind>] [-Tenant <Guid>] [-UserNames <String>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------EXAMPLE--------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication
```

```
$crawlLogPermission = Get-SPEnterpriseSearchCrawlLogReadPermission -SearchApplication $ssa -Tenant "00000000-0000-0000-0000-000000000001"
```

```
Remove-SPEnterpriseSearchCrawlLogReadPermission -Identity $crawlLogPermission -UserNames "contoso\user1;contoso\user2"
```

This example removes user1 and user2 from the list of users referenced by **$crawlLogPermission**. **$crawlLogPermission** is the list of users who have permission to view the crawl log information from the tenant with id "00000000-0000-0000-0000-000000000001" on the search application referenced by **$ssa**. 
  
## Detailed Description

Only the Search Service Application administrator can use this cmdlet. 
  
The **Remove-SPEnterpriseSearchCrawlLogReadPermission** cmdlet removes the permission to view crawl log information for one or more users. The administrator can choose to restrict this removal to a particular tenant. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawlLogReadPermissionPipeBind  <br/> |Specifies the crawl log permissions list from which to remove the user(s).  <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the crawl log. The type must be a valid GUID, of the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _Tenant_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies the tenant for which the user permissions shall be removed. The type must be a valid GUID of the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _UserNames_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the user names that shall no longer have permission to view the crawl log information. Separate names with semi-colons.  <br/> Specifies the user names that no longer shall have permission to view the crawl log information. Use the form "domain\username". When adding several user names, separate names with semi-colons.  <br/> |
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

[Set-SPEnterpriseSearchCrawlLogReadPermission](set-spenterprisesearchcrawllogreadpermission.md)
  
[Get-SPEnterpriseSearchCrawlLogReadPermission](get-spenterprisesearchcrawllogreadpermission.md)

