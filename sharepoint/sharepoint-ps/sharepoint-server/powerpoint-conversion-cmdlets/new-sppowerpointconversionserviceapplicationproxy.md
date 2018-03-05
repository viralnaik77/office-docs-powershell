---
title: "New-SPPowerPointConversionServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 029c4e03-a7c7-4d43-b9c7-ae28a1f0f770

description: "Creates a PowerPoint Conversion Service application proxy."
---

# New-SPPowerPointConversionServiceApplicationProxy

Creates a PowerPoint Conversion Service application proxy. 
  
```
New-SPPowerPointConversionServiceApplicationProxy [-Name] <String> -ServiceApplication <SPPowerPointConversionServiceApplicationPipeBind> [-AddToDefaultGroup <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **New-SPPowerPointConversionServiceApplicationProxy** cmdlet to create a PowerPoint Conversion Service application proxy. The service application proxy is instantiated on the front-end web server and acts as an intermediary between the client computer and the service application back end. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the service application proxy.  <br/> |
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Server.PowerPoint.PowerShell.SPPowerPointConversionServiceApplicationPipeBind  <br/> |Specifies the name of the service application to bind.  <br/> |
|**AddToDefaultGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Adds the newly created proxy to the default service application proxy group. If not specified, the proxy is not added to a group.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Server.PowerPoint.PowerShell.SPPowerPointConversionServiceApplicationPipeBind  <br/> ||
|**AddToDefaultGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------EXAMPLE--------- 
  
```
New-SPPowerPointConversionServiceApplicationProxy -Name "MyWorkgroupPPTAppProxy" -ServiceApplication "MyWorkgroupPPTApp" -AddtoDefaultGroup
```

This example creates a new instance of the PowerPoint Conversion Service application proxy named **MyWorkgroupPPTAppProxy**, binds it to the MyWorkgroupPPTApp service application, and then adds it to the default service application proxy group 
  
## See also

#### 

[New-SPPowerPointConversionServiceApplication](new-sppowerpointconversionserviceapplication.md)
  
[Set-SPPowerPointConversionServiceApplication](set-sppowerpointconversionserviceapplication.md)

