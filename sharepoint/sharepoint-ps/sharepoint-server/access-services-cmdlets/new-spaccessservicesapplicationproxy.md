---
title: "New-SPAccessServicesApplicationProxy"
ms.author: kirks
author: Techwriter40
ms.date: 10/20/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: b8989177-f073-4bc9-b6e3-de829226071c

description: "Enables the creation of a new proxy for a target Access Services Application."
---

# New-SPAccessServicesApplicationProxy

Enables the creation of a new proxy for a target Access Services Application.
  
```
New-SPAccessServicesApplicationProxy -application <SPServiceApplication> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

-----------EXAMPLE--------
  
```
$serviceApp = Get-SPServiceApplication -Name "Access Services"
```

```
New-SPAccessServicesApplicationProxy -application $serviceApp
```

This example gets a Access Services services application named  `Access Services`, and then creates a Access Services application proxy.
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _application_ <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPServiceApplication  <br/> |Specifies the SPServiceApplication of type Access Services.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[New-SPAccessServicesApplication](new-spaccessservicesapplication.md)

