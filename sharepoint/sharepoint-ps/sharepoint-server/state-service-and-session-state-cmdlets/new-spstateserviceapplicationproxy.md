---
title: "New-SPStateServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f20db78d-5f88-4ac1-85d8-5a2809bacefb

description: "Creates a proxy for a state service application."
---

# New-SPStateServiceApplicationProxy

Creates a proxy for a state service application.
  
```
New-SPStateServiceApplicationProxy [-ServiceApplication] <SPStateServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-DefaultProxyGroup <SwitchParameter>] [-Name <String>]
```

## Detailed Description

The **New-SPStateServiceApplicationProxy** cmdlet creates a proxy for a state service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Administration.SPStateServiceApplicationPipeBind  <br/> |Specifies the state service application to associate with the new proxy.  <br/> The type must be a valid name of a state service application (for example, StateServiceApp1); a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid **SPStateServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the service application proxy is added to the farm's default proxy group.  <br/> |
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the display name of the new proxy.  <br/> The type must be a valid name of a SQL Server database; for example, SessionStateDB1. Service application proxy; for example, StateSvcAppProxy1.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Administration.SPStateServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

--------------EXAMPLE-------------------
  
```
Get-SPServiceApplication -Identity 9703f7e2-9521-47c3-bd92-80e3eeba391b | New-SPStateServiceApplicationProxy -DefaultProxyGroup
```

This example creates a new service application proxy, associates it with a provided service application, and adds it to the farm's default proxy group.
  
## See also

#### 

[Get-SPStateServiceApplicationProxy](get-spstateserviceapplicationproxy.md)
  
[Set-SPStateServiceApplicationProxy](set-spstateserviceapplicationproxy.md)

