---
title: "New-SPVisioServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a113b2ab-6a21-47b1-a526-e2f6fc43efc0

description: "Adds a new Visio Services application proxy to a farm."
---

# New-SPVisioServiceApplicationProxy

Adds a new Visio Services application proxy to a farm.
  
```
New-SPVisioServiceApplicationProxy -ServiceApplication <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Name <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **New-SPVisioServiceApplicationProxy** cmdlet adds a new Visio Services application proxy to a farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceApplication** <br/> |Required  <br/> |System.String  <br/> |Specifies the Visio Services application that is associated with the application proxy.  <br/> The type must be a valid name of a Visio Services application; for example, MyVisioService1.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Name** <br/> |Optional  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationProxyPipeBind  <br/> |Specifies the Visio Services application proxy to create.  <br/> The type must be a valid name of a Visio Services application; for example, MyVisioService1.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceApplication** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------------EXAMPLE------------------------ 
  
```
New-SPVisioServiceApplicationProxy -Name "ProxyToVGS3" -ServiceApplication "VGS3"
```

This example creates a new Visio Services application proxy connected to a Visio Services application.
  
## See also

#### 

[Get-SPVisioServiceApplicationProxy](get-spvisioserviceapplicationproxy.md)

