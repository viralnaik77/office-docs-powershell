---
title: "New-SPVisioServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e1dcb38a-69ad-4960-a312-a5831ca9cb90

description: "Adds a new Visio Services application to a farm."
---

# New-SPVisioServiceApplication

Adds a new Visio Services application to a farm.
  
```
New-SPVisioServiceApplication -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> [-CreateDefaultProxy] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Name <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **New-SPVisioServiceApplication** cmdlet adds a new Visio Services application to a farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the existing IIS application pool in which to run the Web service for the service application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an application pool (for example, AppPoolName1); or an instance of a valid **IISWebServiceApplicationPool** object.  <br/> |
|**CreateDefaultProxy** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that a default proxy is created for the new Visio Services application.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Name** <br/> |Optional  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> |Specifies the Visio Services application to create.  <br/> The type must be a valid name of a Visio Service application; for example, MyVisioService1.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**AddToDefaultGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

----------------EXAMPLE 1---------------------
  
```
New-SPVisioServiceApplication -Name "VGS2" -ApplicationPool "SharePoint Web Services Default" -CreateDefaultProxy
```

This example creates a new Visio Services application  `VGS2`, and also creates a service application proxy associated with it.
  
----------------EXAMPLE 2---------------------
  
```
Get-SPIISWebServiceApplicationPool "SharePoint Web Services System Default" | New-SPVisioServiceApplication "VGS3"
```

This example creates a new Visio Services application  `VGS3` without creating an associated service application proxy. You can pipe the results from the **Get-SPIISWebServiceApplicationPool** cmdlet. 
  
## See also

#### 

[Get-SPVisioServiceApplication](get-spvisioserviceapplication.md)
  
[Set-SPVisioServiceApplication](set-spvisioserviceapplication.md)

