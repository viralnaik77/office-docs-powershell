---
title: "New-SPWorkflowServiceApplicationProxy"
ms.author: kenwith
author: kenwith
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2186c57e-bb04-4067-a06e-1c21181dfb13

description: "Creates a Workflow Service application proxy."
---

# New-SPWorkflowServiceApplicationProxy

Creates a Workflow Service application proxy.
  
```
New-SPWorkflowServiceApplicationProxy [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-PartitionMode <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **New-SPWorkflowServiceApplicationProxy** cmdlet to create a Workflow Service application proxy that is used to connect SharePoint to an instance of the Workflow Service. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Determines whether a workflow connects the farm to a single workflow service or connects each site subscription to its own workflow service.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------------EXAMPLE-----------
  
```
New-SPWorkflowServiceApplicationProxy -PartitionMode
```

This example creates a WorkFlow Service application proxy with the PartitionMode parameter enabled.
  
## See also

#### 

[Get-SPWorkflowServiceApplicationProxy](get-spworkflowserviceapplicationproxy.md)
  
[Register-SPWorkflowService](register-spworkflowservice.md)

