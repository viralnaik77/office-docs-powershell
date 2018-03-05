---
title: "Disable-SPInfoPathFormTemplate"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1e8e306a-4a37-4fae-a9ef-551c0c9b8b72

description: "Deactivates a InfoPath 2016 form template from the specified site collection."
---

# Disable-SPInfoPathFormTemplate

Deactivates a InfoPath 2016 form template from the specified site collection.
  
```
Disable-SPInfoPathFormTemplate [-Identity] <SPFormTemplatePipeBind> -Site <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Disable-SPInfoPathFormTemplate** cmdlet deactivates the InfoPath 2016 form template that is specified in the **Identity** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPFormTemplatePipeBind  <br/> |Specifies the InfoPath 2016 form template to disable.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a form template (for example, InfoPathFormTemplate1); a valid name of a form template files (for example, FormTemplateFile1.xsn); or an instance of a valid **SPFormTemplate** object.  <br/> |
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the site collection that contains the InfoPath 2016 form template to deactivate.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL, in the form http://server_name; or an instance of a valid **SPSite** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPFormTemplatePipeBind  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------EXAMPLE--------------
  
```
Disable-SPInfoPathFormTemplate -Identity "FormTemplate.xsn" -Site http://testSite
```

```
"FormTemplatexsn" | Disable-SPInfoPathFormTemplate -Site "http://testSite"
```

This example deactivates an InfoPath 2016 form template from a site collection named  `TestSite`.
  
## See also

#### 

[Enable-SPInfoPathFormTemplate](enable-spinfopathformtemplate.md)
  
[Get-SPInfoPathFormTemplate](get-spinfopathformtemplate.md)
  
[Install-SPInfoPathFormTemplate](install-spinfopathformtemplate.md)
  
[Set-SPInfoPathFormTemplate](set-spinfopathformtemplate.md)
  
[Start-SPInfoPathFormTemplate](start-spinfopathformtemplate.md)
  
[Stop-SPInfoPathFormTemplate](stop-spinfopathformtemplate.md)
  
[Test-SPInfoPathFormTemplate](test-spinfopathformtemplate.md)
  
[Uninstall-SPInfoPathFormTemplate](uninstall-spinfopathformtemplate.md)
  
[Update-SPInfoPathFormTemplate](update-spinfopathformtemplate.md)

