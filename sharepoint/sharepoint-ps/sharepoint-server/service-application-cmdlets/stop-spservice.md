---
title: "Stop-SPService"
ms.author: kirks
author: Techwriter40
ms.date: 10/7/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1a2c95e0-4d7a-4c30-870a-d90bdf05d542

description: "Disables a service in the farm."
---

# Stop-SPService

Disables a service in the farm.
  
```
Stop-SPService -Identity <SPServicePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-IncludeCustomServerRole <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------------EXAMPLE 1-----------------
  
```
Stop-SPService -Identity "Microsoft SharePoint Foundation Sandboxed Code Service"
```

This example disables the Microsoft SharePoint Foundation Sandboxed Code Service in the farm.
  
## Detailed Description

The **Stop-SPService** cmdlet disables a service in the farm. Service instances for this service will be stopped on the appropriate servers in the farm. 
  
> [!NOTE]
> This cmdlet only controls service instances on servers that are managed by MinRole. The behavior for the Custom server role has changed with the November 2016 Public Update (PU). Please see the **IncludeCustomServerRole** parameter for additional information. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServicePipeBind  <br/> |Specifies the name of the service to disable.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _IncludeCustomServerRole_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Creates a timer job that also stops service instances on servers that are assigned to the custom server role.  <br/> > [!NOTE]> This is a one-time Timer job. MinRole will make no further attempts to manage the service instances on servers assigned to the Custom server role.           |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Get-SPService](get-spservice.md)
  
[Start-SPService](start-spservice.md)

