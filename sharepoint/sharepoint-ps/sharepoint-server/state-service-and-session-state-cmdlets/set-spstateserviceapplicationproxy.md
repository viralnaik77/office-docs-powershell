---
title: "Set-SPStateServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2a6b90d6-c124-448f-9c25-a98111b4be14

description: "Updates the name of a state service application proxy."
---

# Set-SPStateServiceApplicationProxy

Updates the name of a state service application proxy.
  
```
Set-SPStateServiceApplicationProxy [-Identity] <SPStateServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Name <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPStateServiceApplicationProxy** cmdlet updates the name of a state service application proxy. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Administration.SPStateServiceApplicationProxyPipeBind  <br/> |Specifies the state service application proxy to update.  <br/> The type must be a valid name of a state service application proxy (for example, StateServiceProxy); a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid **SPStateServiceApplicationProxy** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the display name of the state service application proxy.  <br/> The type must be a valid name of a state service application; for example, StateSvcProxy1.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Administration.SPStateServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Set-SPServiceApplicationProxy -Identity 9703f7e2-9521-47c3-bd92-80e3eeba391b -Name "New Service Application Proxy Name"
```

This example changes the display name of a state service application proxy.
  
## See also

#### 

[Get-SPStateServiceApplicationProxy](get-spstateserviceapplicationproxy.md)
  
[New-SPStateServiceApplicationProxy](new-spstateserviceapplicationproxy.md)

