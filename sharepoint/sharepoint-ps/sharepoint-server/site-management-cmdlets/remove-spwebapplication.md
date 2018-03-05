---
title: "Remove-SPWebApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9e9fca0-403a-4071-83ee-2cf7bdab0ed3

description: "Deletes the specified Web application."
---

# Remove-SPWebApplication

Deletes the specified Web application.
  
```
Remove-SPWebApplication [-Identity] <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DeleteIISSite <SwitchParameter>] [-RemoveContentDatabases <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Remove-SPWebApplication** cmdlet deletes the Web application specified by the **Identity** and **Zone** parameters. If no zone is provided, the entire Web application and all zones are removed. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the URL or name of the Web application to delete.  <br/> The type must be a valid URL, in the form http://server_name, or a valid name, in the form WebApplication-1212.  <br/> |
|**Zone** <br/> |Required  <br/> |System.String  <br/> |Specifies one of the five zones to be removed. If this parameter is not provided, all Web application zones are removed.  <br/> The type must be any one of the following values: **Default**, **Intranet**, **Internet**, **Extranet**, or **Custom**.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DeleteIISSite** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Deletes the associated IIS Web sites. If this parameter is not provided, the IIS site is not removed.  <br/> |
|**RemoveContentDatabases** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Permanently deletes all associated content databases. If this parameter is not provided, no content databases are removed.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**Zone** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DeleteIISSite** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**RemoveContentDatabases** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1-----------------------
  
```
Get-SPWebApplication http://sitename | Remove-SPWebApplication -Zone "Internet" -Confirm
```

This example prompts and then removes the  `Internet` zone Web application extension on the Web application at  `http://sitename`. This command does not remove the content databases or the IIS Web site.
  
------------------EXAMPLE 2-----------------------
  
```
Remove-SPWebApplication http://sitename -Confirm -DeleteIISSite -RemoveContentDatabases
```

This example permanently removes the Web application, all content databases, and the IIS Web site at  `http://sitename`
  
## See also

#### 

[Get-SPWebApplication](get-spwebapplication.md)
  
[Set-SPWebApplication](set-spwebapplication.md)
  
[New-SPWebApplication](new-spwebapplication.md)

