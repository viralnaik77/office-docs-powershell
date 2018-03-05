---
title: "Upgrade-SPEnterpriseSearchServiceApplication"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d864545d-2b27-4cc0-9c56-e421fb8d0641

description: "Upgrades a search service application."
---

# Upgrade-SPEnterpriseSearchServiceApplication

Upgrades a search service application.
  
```
Upgrade-SPEnterpriseSearchServiceApplication -Identity <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

----------------EXAMPLE 1-----------------
  
```
Get-SPEnterpriseSearchServiceApplication | Upgrade-SPEnterpriseSearchServiceApplication
```

This example upgrades a search service application.
  
----------------EXAMPLE 2-----------------
  
```
Upgrade-SPEnterpriseSearchServiceApplication -Identity 846ceb0b-31d6-4c79-82c1-3a9deafe0b45
```

This example upgrades a search service application.
  
----------------EXAMPLE 3-----------------
  
```
Upgrade-SPEnterpriseSearchServiceApplication "DefaultSearchApplication"
```

This example upgrades a search service application.
  
## Detailed Description

This cmdlet starts an upgrade process on a search service application. This cmdlet runs the associated upgrade actions for the search service application. Also, you can upgrade multiple search service applications in parallel by starting several instances of this cmdlet. It is not necessary to run this cmdlet if you already have run the SharePoint Products Configuration Wizard.
  
> [!NOTE]
> For the upgrade process to run successful, all of the computers in the farm must have the same version of binaries installed. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search service application to upgrade.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchServiceApplication](new-spenterprisesearchserviceapplication.md)
  
[Get-SPEnterpriseSearchServiceApplication](get-spenterprisesearchserviceapplication.md)
  
[Remove-SPEnterpriseSearchServiceApplication](remove-spenterprisesearchserviceapplication.md)
  
[Restore-SPEnterpriseSearchServiceApplication](restore-spenterprisesearchserviceapplication.md)
  
[Set-SPEnterpriseSearchServiceApplication](set-spenterprisesearchserviceapplication.md)
  
[Suspend-SPEnterpriseSearchServiceApplication](suspend-spenterprisesearchserviceapplication.md)
  
[Resume-SPEnterpriseSearchServiceApplication](resume-spenterprisesearchserviceapplication.md)

