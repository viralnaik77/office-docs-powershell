---
title: "New-SPManagedPath"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d30deac-e368-4137-89b5-a20c0785b2a4

description: "Creates a new managed path for the given Web application for all host header site collections."
---

# New-SPManagedPath

Creates a new managed path for the given Web application for all host header site collections.
  
```
New-SPManagedPath [-RelativeURL] <String> -WebApplication <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Explicit <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **New-SPManagedPath** cmdlet adds a new managed path to a given Web application or for use with all host header site collections. If the **HostHeader** switch is provided, the managed path is shared among all host header site collections; otherwise, a Web application must be specified to create this managed path within. The relative URL is a partial URL that represents the managed path. When the slash mark (/) is used, the root is defined. If the **Explicit** parameter is not provided, the new managed path is a wildcard path. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**RelativeURL** <br/> |Required  <br/> |System.String  <br/> |Specifies the relative URL for the new managed path.  <br/> The type must be a valid partial URL such as **site** or **sites/teams/.** <br/> |
|**HostHeader** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |If this parameter is provided, this managed path applies to all host header site collections.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the Web application group to add this path.  <br/> The type must be a valid URL, in the form http://server_name, or a GUID, in the form 1234-5678-0987645a.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Explicit** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether the managed path is explicit or wildcard.  <br/> If not provided, the managed path is a wildcard path.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**RelativeURL** <br/> |Required  <br/> |System.String  <br/> ||
|**HostHeader** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Explicit** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
New-SPManagedPath "Teams" -WebApplication "http://somesite"
```

This example creates a  `Teams` managed path for a given Web application (  `http://somesite`).
  
## See also

#### 

[Get-SPManagedPath](get-spmanagedpath.md)
  
[Remove-SPManagedPath](remove-spmanagedpath.md)

