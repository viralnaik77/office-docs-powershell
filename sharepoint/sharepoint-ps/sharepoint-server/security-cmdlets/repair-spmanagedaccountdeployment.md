---
title: "Repair-SPManagedAccountDeployment"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 42ea7573-8b34-49da-9d7f-ec7b8211a138

description: "Repairs the local managed account credential deployment."
---

# Repair-SPManagedAccountDeployment

Repairs the local managed account credential deployment.
  
```
Repair-SPManagedAccountDeployment [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Repair-SPManagedAccountDeployment** cmdlet to repair the local deployment of managed account credentials deployment on a server for the rare cases that the managed accounts service credentials are in a broken state. It re-deploys each local service and Web applications credentials and also determines if the passphrase is not correct on the server and repairs provides warnings accordingly. The **Repair-SPManagedAccountDeployment** cmdlet should not be used as part of the regular credential update process, but should be one of the first troubleshooting steps, specifically if a servers' services are failing to start when other servers' services are working correctly. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

----------EXAMPLE----------- 
  
```
Repair-SPManagedAccountDeployment
```

This example repairs the deployment of credentials on all services and Web application associated with managed account (s) on the local server.
  

