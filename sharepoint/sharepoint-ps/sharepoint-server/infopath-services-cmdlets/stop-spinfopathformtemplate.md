---
title: "Stop-SPInfoPathFormTemplate"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b2795395-f293-4b17-aa1b-64ec46fb6856

description: "Disables a InfoPath 2016 form template on a farm before an upgrade."
---

# Stop-SPInfoPathFormTemplate

Disables a InfoPath 2016 form template on a farm before an upgrade.
  
```
Stop-SPInfoPathFormTemplate -Identity <SPFormTemplatePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-TimeLeft <Int32>] [-WhatIf [<SwitchParameter>]]

```

## Example

---------------EXAMPLE--------------
  
```
Stop-SPInfoPathFormTemplate -Identity formName.xsn
```

This example disables a form template for a specified name.
  
## Detailed Description

The **Stop-SPInfoPathFormTemplate** cmdlet quiesces, or disables, an InfoPath 2016 form template before it upgrades the form. Before a form is updated it is quiesced, which disables access to the form. Use **Start-SPIPFormTemplate** to unquiesce, or activate, a form template after the form is upgraded. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPFormTemplatePipeBind  <br/> |Specifies the InfoPath 2016 form template to start.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a form template (for example, InfoPathFormTemplate1); a valid name of a form template files (for example, FormTemplateFile1.xsn); or an instance of a valid **SPFormTemplate** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _TimeLeft_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the time duration, in minutes, before the form template will be quiesced. The default value is **0**.  <br/> An integer value in the range from 0 to 1440.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPFormTemplatePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**TimeLeft** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Disable-SPInfoPathFormTemplate](disable-spinfopathformtemplate.md)
  
[Enable-SPInfoPathFormTemplate](enable-spinfopathformtemplate.md)
  
[Get-SPInfoPathFormTemplate](get-spinfopathformtemplate.md)
  
[Install-SPInfoPathFormTemplate](install-spinfopathformtemplate.md)
  
[Set-SPInfoPathFormTemplate](set-spinfopathformtemplate.md)
  
[Start-SPInfoPathFormTemplate](start-spinfopathformtemplate.md)
  
[Test-SPInfoPathFormTemplate](test-spinfopathformtemplate.md)
  
[Uninstall-SPInfoPathFormTemplate](uninstall-spinfopathformtemplate.md)
  
[Update-SPInfoPathFormTemplate](update-spinfopathformtemplate.md)

