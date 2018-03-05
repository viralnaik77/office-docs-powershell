---
title: "Set-SPVisioServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14558051-32d7-4a71-be8c-4137ccc7fed4

description: "Sets the ServiceApplicationPool property for a Visio Services application."
---

# Set-SPVisioServiceApplication

Sets the **ServiceApplicationPool** property for a Visio Services application. 
  
```
Set-SPVisioServiceApplication [-Identity] <SPVisioServiceApplicationPipeBind> [-ServiceApplicationPool] <SPIisWebServiceApplicationPoolPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPVisioServiceApplication** cmdlet sets the **ServiceApplicationPool** property for a Visio Services application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> |Specifies the Visio Services application to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a Visio Services application (for example, MyVisioService1); or an instance of a valid **SPVisioServiceApplication** object.  <br/> |
|**ServiceApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the IIS application pool to change. The Web service for the service application runs in the specified application pool.  <br/> The type must be a valid name of a Visio Service application pool, such as MyVisioServiceAppPool1; or a valid GUID, such as 12345678-90ab-cdef-1234-567890bcdefgh, or an instance of a valid **SPIisWebServiceApplicationPoolPipeBind** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> ||
|**ServiceApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------------EXAMPLE 1----------------------
  
```
Set-SPVisioServiceApplication -identity "VGS1" -ServiceApplicationPool "SharePoint Web Services System Default"
```

This example changes the application pool of the  `VGS1` service application. 
  
-----------------EXAMPLE 2----------------------
  
```
Get-SPServiceApplicationPool "SharePoint Web Services Default" | Set-SPVisioServiceApplication VGS1
```

This example changes the application pool of the  `VGS1` service application. The results are piped from the **Get-SPServiceApplicationPool** cmdlet. 
  
## See also

#### 

[New-SPVisioServiceApplication](new-spvisioserviceapplication.md)
  
[Get-SPVisioServiceApplication](get-spvisioserviceapplication.md)
  
[Get-SPVisioServiceApplication](get-spvisioserviceapplication.md)

