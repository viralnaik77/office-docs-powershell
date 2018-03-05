---
title: "Remove-SPEnterpriseSearchServiceApplication"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc851e8-bf01-4b46-b0d6-f2deb7c6e0b7

description: "Deletes a search service application."
---

# Remove-SPEnterpriseSearchServiceApplication

Deletes a search service application.
  
```
Remove-SPEnterpriseSearchServiceApplication -Identity <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-RemoveData <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
Remove-SPEnterpriseSearchServiceApplication -Identity MySSA
```

This example removes the search service application named  `MySSA` from the farm. 
  
## Detailed Description

This cmdlet deletes a specified **SearchServiceApplication** from a farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search service application to delete.  <br/> A valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _RemoveData_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that all search databases and index files associated with the search service application to be deleted.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**RemoveData** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchServiceApplication](new-spenterprisesearchserviceapplication.md)
  
[Get-SPEnterpriseSearchServiceApplication](get-spenterprisesearchserviceapplication.md)
  
[Set-SPEnterpriseSearchServiceApplication](set-spenterprisesearchserviceapplication.md)
  
[Restore-SPEnterpriseSearchServiceApplication](restore-spenterprisesearchserviceapplication.md)
  
[Upgrade-SPEnterpriseSearchServiceApplication](upgrade-spenterprisesearchserviceapplication.md)
  
[Suspend-SPEnterpriseSearchServiceApplication](suspend-spenterprisesearchserviceapplication.md)
  
[Resume-SPEnterpriseSearchServiceApplication](resume-spenterprisesearchserviceapplication.md)

