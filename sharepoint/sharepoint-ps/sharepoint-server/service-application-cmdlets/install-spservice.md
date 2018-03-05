---
title: "Install-SPService"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 7/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: 6a7b8a23-85ba-4609-83bf-d8672f5b25b4

description: "Installs and provisions services on a farm."
---

# Install-SPService

Installs and provisions services on a farm.
  
```
Install-SPService [-AssignmentCollection <SPAssignmentCollection>] [-Provision <SwitchParameter>]
```

## Detailed Description

The **Install-SPService** cmdlet installs and optionally provisions services on a farm. This cmdlet installs all services, service instances, and service proxies specified in the registry on the local server computer. Use this cmdlet in a script that you build to install and deploy a SharePoint farm or to install a custom developed service. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Provision** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies default settings when installing a standalone service application.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Provision** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Install-SPService
```

This example installs all services, service instances and service proxies specified in the registry on the local server computer.
  

