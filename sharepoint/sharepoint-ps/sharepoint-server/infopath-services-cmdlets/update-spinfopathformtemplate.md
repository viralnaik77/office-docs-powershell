---
title: "Update-SPInfoPathFormTemplate"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7095759f-3b6c-4279-a8b1-24a3174185e5

description: "Upgrades all InfoPath form templates on the farm."
---

# Update-SPInfoPathFormTemplate

Upgrades all InfoPath form templates on the farm.
  
```
Update-SPInfoPathFormTemplate [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Update-SPInfoPathFormTemplate** cmdlet upgrades all the InfoPath form templates on a farm that were deployed by an administrator. Use this cmdlet after the farm is upgraded to a new version. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------EXAMPLE--------------
  
```
Update-SPInfoPathFormTemplate
```

This example updates InfoPath form templates on the entire farm.
  
## See also

#### 

[Disable-SPInfoPathFormTemplate](disable-spinfopathformtemplate.md)
  
[Enable-SPInfoPathFormTemplate](enable-spinfopathformtemplate.md)
  
[Get-SPInfoPathFormTemplate](get-spinfopathformtemplate.md)
  
[Install-SPInfoPathFormTemplate](install-spinfopathformtemplate.md)
  
[Set-SPInfoPathFormTemplate](set-spinfopathformtemplate.md)
  
[Start-SPInfoPathFormTemplate](start-spinfopathformtemplate.md)
  
[Stop-SPInfoPathFormTemplate](stop-spinfopathformtemplate.md)
  
[Test-SPInfoPathFormTemplate](test-spinfopathformtemplate.md)
  
[Uninstall-SPInfoPathFormTemplate](uninstall-spinfopathformtemplate.md)

