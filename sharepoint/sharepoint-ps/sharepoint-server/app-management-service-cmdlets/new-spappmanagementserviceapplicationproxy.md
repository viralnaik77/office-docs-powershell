---
title: "New-SPAppManagementServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/20/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 73327d12-9675-47bf-9c36-4290383a83c9

description: "Creates an App Management Service application proxy."
---

# New-SPAppManagementServiceApplicationProxy

Creates an App Management Service application proxy.
  
```
New-SPAppManagementServiceApplicationProxy -Uri <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Name <String>] [-UseDefaultProxyGroup <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **New-SPAppManagementServiceApplicationProxy** cmdlet to create an App Management Service application proxy with the specified name for the specified App Management Service application or the specified endpoint. Depending on the parameter value, it also adds the new proxy to the default proxy group. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> |Specifies the App Management Service application for which you are creating the service application proxy.  <br/> |
|**Uri** <br/> |Required  <br/> |System.String  <br/> |Specifies the endpoint URI of the App Management Service application in which to create the service application proxy.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the service application proxy to be created. If a value is not provided, a default name is used.  <br/> |
|**UseDefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether to add the newly created service application proxy to the default proxy group.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**Uri** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**UseDefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------EXAMPLE------------- 
  
```
$appManagementServiceApplication= 
```

```
New-SPAppManagementServiceApplicationProxy -Name AppManagementProxy -UseDefaultProxyGroup -ServiceApplication $appManagementServiceApplication
```

This example creates a new App Management Service application proxy named **AppManagementProxy** for the specified service application and adds the new App Management Service application proxy to the default proxy group. 
  
## See also

#### 

[New-SPAppManagementServiceApplication](new-spappmanagementserviceapplication.md)

