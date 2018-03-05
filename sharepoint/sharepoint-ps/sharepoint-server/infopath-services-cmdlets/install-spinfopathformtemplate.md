---
title: "Install-SPInfoPathFormTemplate"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b99f33e3-6f2b-43e0-9a35-1aea11337dfe

description: "Installs an InfoPath 2016 form template on a farm."
---

# Install-SPInfoPathFormTemplate

Installs an InfoPath 2016 form template on a farm.
  
```
Install-SPInfoPathFormTemplate [-Path] <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-EnableGradualUpgrade <SwitchParameter>] [-NoWait <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Install-SPInfoPathFormTemplate** cmdlet installs an InfoPath 2016 form template on a farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies the path and name of the form template to install.  <br/>  The type must be a valid path and file name of a form template, in the form:  <br/> - C:\folder_name\formtemplate_name  <br/> - \\server_name\folder_name\formtemplate_name  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**EnableGradualUpgrade** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the new form can be gradually upgraded.  <br/> - If specified and the form template file exists, the form template is gradually upgraded and is then used for new sessions only.  <br/> - If not specified and the form template does not exist, the form is overwritten during an upgrade and is then used for exisiting and new sessions.  <br/> - If specified and the form template file does not exist, ignore the switch.  <br/> - If not specified and the file exists, the user is prompted to upgrade and to use the gradual upgrade if the upgrade is allowed.  <br/> |
|**NoWait** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the form template is installed in the background and that the progress of the installation not be shown.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**EnableGradualUpgrade** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**NoWait** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------EXAMPLE--------------
  
```
Install-SPInfoPathFormTemplate -Path c:\Form.xsn
```

```
"FormTemplateFirst.xsn", "FormTemplateSecond.xsn", "FormTemplateThird.xsn" | Install-SPInfoPathFormTemplate
```

This example installs multiple form templates on a farm.
  
## See also

#### 

[Disable-SPInfoPathFormTemplate](disable-spinfopathformtemplate.md)
  
[Enable-SPInfoPathFormTemplate](enable-spinfopathformtemplate.md)
  
[Get-SPInfoPathFormTemplate](get-spinfopathformtemplate.md)
  
[Set-SPInfoPathFormTemplate](set-spinfopathformtemplate.md)
  
[Start-SPInfoPathFormTemplate](start-spinfopathformtemplate.md)
  
[Stop-SPInfoPathFormTemplate](stop-spinfopathformtemplate.md)
  
[Test-SPInfoPathFormTemplate](test-spinfopathformtemplate.md)
  
[Uninstall-SPInfoPathFormTemplate](uninstall-spinfopathformtemplate.md)
  
[Update-SPInfoPathFormTemplate](update-spinfopathformtemplate.md)

