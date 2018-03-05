---
title: "Remove-SPWeb"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9bc8078-626a-4838-b12b-21f1bb832935

description: "Completely deletes the specified Web."
---

# Remove-SPWeb

Completely deletes the specified Web.
  
```
Remove-SPWeb [-Identity] <SPWebPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Recycle <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPWeb** cmdlet completely deletes the Web specified by the **Identity** parameter. 
  
> [!IMPORTANT]
> Deleting the top level Web site of a site collection causes the entire site collection to be removed. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the identity of the Web to delete.  <br/> The type must be a valid full URL, in the form http://server_name/site_name, or an **SPWeb** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Recycle** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies if the **SPWeb** object should be recycled.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Recycle** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
Remove-SPWeb http://sitename/subsite
```

This example completely deletes a  `subsite`.
  
## See also

#### 

[Get-SPWeb](get-spweb.md)
  
[Set-SPWeb](set-spweb.md)
  
[Remove-SPWeb](remove-spweb.md)
  
[New-SPWeb](new-spweb.md)
  
[Import-SPWeb](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/import-and-export-cmdlets/import-spweb.md)

