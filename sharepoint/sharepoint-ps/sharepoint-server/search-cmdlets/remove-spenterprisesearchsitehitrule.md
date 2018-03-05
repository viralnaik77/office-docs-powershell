---
title: "Remove-SPEnterpriseSearchSiteHitRule"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5551df7f-5f62-4c67-ae59-96b89e95a60a

description: "Deletes a site hit rule."
---

# Remove-SPEnterpriseSearchSiteHitRule

Deletes a site hit rule.
  
```
Remove-SPEnterpriseSearchSiteHitRule -Identity <SiteHitRulePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-SearchService <SearchServicePipeBind>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE-------------------
  
```
Remove-SPEnterpriseSearchSiteHitRule -Identity myHost
```

This example removes a site hit rule for the  `myHost` host. 
  
## Detailed Description

The **Remove-SPEnterpriseSearchSiteHitRule** cmdlet deletes the site hit rule that controls the number of threads used to crawl a given site. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SiteHitRulePipeBind  <br/> |The rule that is used for the specified site.  <br/> The type must be a valid site hit rule host or an instance of a valid **SiteHitRule** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _SearchService_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServicePipeBind  <br/> |Specifies the search service in the farm that hosts the crawl.  <br/> The type must be an instance of a valid **SearchService** object; otherwise, the local service on the server that hosts the Windows PowerShell cmdlet is used.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SiteHitRulePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SearchService** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServicePipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchSiteHitRule](get-spenterprisesearchsitehitrule.md)
  
[New-SPEnterpriseSearchSiteHitRule](new-spenterprisesearchsitehitrule.md)

