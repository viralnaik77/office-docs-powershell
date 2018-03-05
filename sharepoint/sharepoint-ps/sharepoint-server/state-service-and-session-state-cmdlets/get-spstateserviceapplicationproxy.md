---
title: "Get-SPStateServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4ecf5816-5d8d-4ea6-85dd-7b09770b821f

description: "Returns state service application proxies on the farm."
---

# Get-SPStateServiceApplicationProxy

Returns state service application proxies on the farm.
  
```
Get-SPStateServiceApplicationProxy [[-Identity] <SPStateServiceApplicationProxyPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Get-SPStateServiceApplicationProxy** cmdlet returns a state service application proxy on the farm. If the **Identity** parameter is not specified, this cmdlet returns the collection of all state service application proxies on the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Administration.SPStateServiceApplicationProxyPipeBind  <br/> |Specifies the state service application proxy to get.  <br/> The type must be a valid name of a state service application proxy (for example, StateServiceProxy); a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Administration.SPStateServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------EXAMPLE 1-----------------
  
```
Get-SPStateServiceApplicationProxy
```

This example displays all the state service application proxies on the farm.
  
--------------EXAMPLE 2-----------------
  
```
Get-SPStateServiceApplicationProxy -Identity 81dc50e0-c0f9-4d2c-8284-bb03bb1ea676
```

This example displays a specific state service application proxy on the farm.
  
## See also

#### 

[New-SPStateServiceApplicationProxy](new-spstateserviceapplicationproxy.md)
  
[Set-SPStateServiceApplicationProxy](set-spstateserviceapplicationproxy.md)

