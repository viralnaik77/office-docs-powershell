---
title: "Remove-SPEnterpriseSearchServiceApplicationProxy"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a2d77879-9aa7-4986-abc1-051a59dfda59

description: "Deletes a search service application proxy."
---

# Remove-SPEnterpriseSearchServiceApplicationProxy

Deletes a search service application proxy.
  
```
Remove-SPEnterpriseSearchServiceApplicationProxy -Identity <SearchServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
Remove-SPEnterpriseSearchServiceApplicationProxy -Identity SearchProxy
```

This example removes a search service application proxy named  `SearchProxy`.
  
## Detailed Description

This cmdlet deletes the specified search service application proxy from a farm.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationProxyPipeBind  <br/> |Specifies the search service application proxy to delete.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a service application proxy (for example, ServiceAppProxy1); or an instance of a valid **SearchServiceApplicationProxy** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchServiceApplicationProxy](get-spenterprisesearchserviceapplicationproxy.md)
  
[Set-SPEnterpriseSearchServiceApplicationProxy](set-spenterprisesearchserviceapplicationproxy.md)
  
[New-SPEnterpriseSearchServiceApplicationProxy](new-spenterprisesearchserviceapplicationproxy.md)

