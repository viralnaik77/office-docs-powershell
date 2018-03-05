---
title: "Get-SPService"
ms.author: kirks
author: Techwriter40
ms.date: 3/28/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b11a95b-afb6-4496-adcc-cc4d3365d2bd

description: "Gets a service in the farm."
---

# Get-SPService

Gets a service in the farm.
  
```
Get-SPService [-Identity <SPServicePipeBind>] [-All <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>]

```

## Detailed Description

The **Get-SPService** cmdlet gets a service in the farm. 
  
## Example

--------------EXAMPLE 1-----------------
  
```
Get-SPService -Identity "Microsoft SharePoint Server Diagnostics Service"
```

This example gets the Microsoft SharePoint Server Diagnostics Service in the farm. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _All_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies all services in the farm.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServicePipeBind  <br/> |Specifies the name of the service to get.  <br/> |
   
## See also

#### 

[Start-SPService](start-spservice.md)
  
[Stop-SPService](stop-spservice.md)

