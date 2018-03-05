---
title: "New-SPEnterpriseSearchSiteHitRule"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 2/18/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b7a7b3f5-bc2c-4592-9168-7ff465768e79

description: "Adds a new site hit rule for a search application."
---

# New-SPEnterpriseSearchSiteHitRule

Adds a new site hit rule for a search application.
  
```
New-SPEnterpriseSearchSiteHitRule -Behavior <String> -HitRate <String> -Name <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-SearchService <SearchServicePipeBind>] [-WhatIf [<SwitchParameter>]]

```

## Example

----------------EXAMPLE------------------
  
```
New-SPEnterpriseSearchSiteHitRule -Name myHost -Behavior 0 -HitRate 40
```

This example creates a new site hit rule on the  `myHost` host that limits to  `40` the number of simultaneous requests. 
  
## Detailed Description

The **New-SPEnterpriseSearchSiteHitRule** cmdlet sets the maximum limits for crawling a site. The new site hit rule is used by all search service applications on the current farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Behavior_ <br/> |Required  <br/> |System.String  <br/> |Defines a rule to be followed when the farm's search service crawls the given site. If a value of zero is specified, the hit rate is the maximum number of simultaneous requests. If a value of 1 is specified, then hit rate is the number of seconds to delay between requests to the server.  <br/> |
| _HitRate_ <br/> |Required  <br/> |System.String  <br/> |Value to use for maximum requests or seconds of delay, according to behavior.  <br/> |
| _Name_ <br/> |Required  <br/> |System.String  <br/> |The name of the host to which the site hit rule should be applied.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _SearchService_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServicePipeBind  <br/> |Specifies the search service in the farm that hosts the crawl.  <br/> The type must be an instance of a valid **SearchService** object; otherwise, the local service on the server that hosts the Windows PowerShell cmdlet will be used.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**Behavior** <br/> |Required  <br/> |System.String  <br/> ||
|**HitRate** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SearchService** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServicePipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchSiteHitRule](get-spenterprisesearchsitehitrule.md)
  
[Remove-SPEnterpriseSearchSiteHitRule](remove-spenterprisesearchsitehitrule.md)

