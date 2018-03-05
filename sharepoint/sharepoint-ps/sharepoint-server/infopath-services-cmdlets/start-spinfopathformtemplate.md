---
title: "Start-SPInfoPathFormTemplate"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 97fee306-a7b1-4761-8ce3-438f5f1814be

description: "Activates a previously quiesced InfoPath 2016 form template."
---

# Start-SPInfoPathFormTemplate

Activates a previously quiesced InfoPath 2016 form template.
  
```
Start-SPInfoPathFormTemplate [-Identity] <SPFormTemplatePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Start-SPInfoPathFormTemplate** cmdlet activates a previously quiesced InfoPath 2016 form template after the form is upgraded. During update, a form is quiesced, which disables access to the form. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPFormTemplatePipeBind  <br/> |Specifies the InfoPath 2016 form template to start.  <br/> The type must be a valid URL, in the form http://server_name; a valid name of a Web application (for example, WebApp1); a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid **SPWebServiceProxy** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPFormTemplatePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------EXAMPLE--------------
  
```
Start-SPInfoPathFormTemplate -Identity formName.xsn
```

This example activates a form with a specified name.
  
## See also

#### 

[Disable-SPInfoPathFormTemplate](disable-spinfopathformtemplate.md)
  
[Enable-SPInfoPathFormTemplate](enable-spinfopathformtemplate.md)
  
[Get-SPInfoPathFormTemplate](get-spinfopathformtemplate.md)
  
[Install-SPInfoPathFormTemplate](install-spinfopathformtemplate.md)
  
[Set-SPInfoPathFormTemplate](set-spinfopathformtemplate.md)
  
[Stop-SPInfoPathFormTemplate](stop-spinfopathformtemplate.md)
  
[Test-SPInfoPathFormTemplate](test-spinfopathformtemplate.md)
  
[Uninstall-SPInfoPathFormTemplate](uninstall-spinfopathformtemplate.md)
  
[Update-SPInfoPathFormTemplate](update-spinfopathformtemplate.md)

