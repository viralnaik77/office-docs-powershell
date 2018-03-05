---
title: "Set-SPEnterpriseSearchServiceApplicationProxy"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 460f7977-117b-4c9b-8085-d97ad30214dd

description: "Sets properties of a search service application proxy."
---

# Set-SPEnterpriseSearchServiceApplicationProxy

Sets properties of a search service application proxy.
  
```
Set-SPEnterpriseSearchServiceApplicationProxy -Identity <SearchServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Name <String>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
Get-SPEnterpriseSearchServiceApplicationProxy -Identity SsaProxy | Set- SPEnterpriseSearchServiceApplicationProxy -Name ContosoSearchProxy
```

This example sets the display name of a search service application proxy.
  
## Detailed Description

This cmdlet updates properties of a site administration service application proxy for a search application. **SPEnterpriseSearchServiceApplicationProxy** represents the proxy for search site administration functionality. One search service application proxy exists for each search application on a farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationProxyPipeBind  <br/> |Specified the search service application proxy to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a search service application proxy (for example, SearchServiceAppProxy1); or an instance of a valid **SearchServiceApplicationProxy** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the display name of the search application proxy to retrieve.  <br/> The type must be a valid string, for example, SearchAppProxy1.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchServiceApplicationProxy](get-spenterprisesearchserviceapplicationproxy.md)
  
[New-SPEnterpriseSearchServiceApplicationProxy](new-spenterprisesearchserviceapplicationproxy.md)
  
[Remove-SPEnterpriseSearchServiceApplicationProxy](remove-spenterprisesearchserviceapplicationproxy.md)

