---
title: "Uninstall-SPDataConnectionFile"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5151855d-0051-4c98-8dc3-ce0843c5a69d

description: "Removes a data connection file."
---

# Uninstall-SPDataConnectionFile

Removes a data connection file.
  
```
Uninstall-SPDataConnectionFile [-Identity] <SPDataConnectionFilePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Uninstall-SPDataConnectionFile** cmdlet removes the data connection file specified in the **Identity** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPDataConnectionFilePipeBind  <br/> |Specifies the data connection file to remove.  <br/> The type must be a valid GUID, in form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a data connection file (for example, DataConnectionFileName1.udcx); or an instance of a valid **SPDataConnectionFile** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPDataConnectionFilePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Uninstall-SPDataConnectionFile -Identity "Sample.udcx
```

```
"Sample1.udcx", "Sample2.udcx", "Sample3.udcx" | Uninstall-SPDataConnectionFile
```

This example uninstalls a specified data connection file in two different ways.
  
## See also

#### 

[Get-SPDataConnectionFile](get-spdataconnectionfile.md)
  
[Install-SPDataConnectionFile](install-spdataconnectionfile.md)
  
[Set-SPDataConnectionFile](set-spdataconnectionfile.md)

