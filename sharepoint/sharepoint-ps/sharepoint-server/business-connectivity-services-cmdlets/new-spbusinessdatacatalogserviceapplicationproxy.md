---
title: "New-SPBusinessDataCatalogServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f73ddc6f-78ca-4736-b827-7df10cad3838

description: "Creates a new Business Data Connectivity service application proxy in the farm."
---

# New-SPBusinessDataCatalogServiceApplicationProxy

Creates a new Business Data Connectivity service application proxy in the farm.
  
```
New-SPBusinessDataCatalogServiceApplicationProxy -Uri <Uri> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DefaultProxyGroup <SwitchParameter>] [-Name <String>] [-PartitionMode <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **New-SPBusinessDataCatalogServiceApplicationProxy** cmdlet creates a new Business Data Connectivity service application proxy for a Business Data Connectivity service application in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies a display name for the new Business Data Connectivity service application proxy.  <br/> |
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> |Specifies the Business Data Connectivity service application associated with the new proxy.  <br/> |
|**Uri** <br/> |Required  <br/> |System.Uri  <br/> |Specifies the URI of a remote service application to which to connect.  <br/> The type must be a valid URI, in the form file:\\server_name\sitedocs.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies if partition mode is to be turned on.  <br/> The valid values are **True** and **False**. The default value is **False**.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the service application proxy is added to the default proxy group for the farm.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**Uri** <br/> |Required  <br/> |System.Uri  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
New-SPBusinessDataCatalogServiceApplicationProxy -Name "ContosoServiceAppProxy" -ServiceApplication $serviceApplication
```

This example creates a new Business Data Connectivity service application proxy with the name  `ContosoServiceAppProxy` for the given service application. 
  
## See also

#### 

[New-SPBusinessDataCatalogServiceApplication](new-spbusinessdatacatalogserviceapplication.md)
  
[Set-SPBusinessDataCatalogServiceApplication](set-spbusinessdatacatalogserviceapplication.md)

