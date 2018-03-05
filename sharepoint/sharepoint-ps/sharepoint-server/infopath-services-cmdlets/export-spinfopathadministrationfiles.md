---
title: "Export-SPInfoPathAdministrationFiles"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d13aee8d-f95b-4544-99bc-09b7c40cd03b

description: "Saves InfoPath 2016 form templates on the SharePoint Central Administration Web site and .udcx files to a .cab file."
---

# Export-SPInfoPathAdministrationFiles

Saves InfoPath 2016 form templates on the SharePoint Central Administration Web site and .udcx files to a .cab file.
  
```
Export-SPInfoPathAdministrationFiles [-Path] <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Identity <SPFormsServicePipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Export-SPInfoPathAdministrationFiles** cmdlet saves all InfoPath 2016 form templates (.xsn files) and universal data connections (.udcx files) that are located on the Central Administration page. The backup package includes all workflow forms in InfoPath that were deployed by an administrator and not included with SharePoint Server 2016, and includes browser forms that were deployed by an administrator. The backup package is output to the specified .cab file. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies the location and name of the output .cab file.  <br/> The type must be a valid file path, in the form \\ipadmin\folder\backups1\ipfsfiles.cab.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPFormsServicePipeBind  <br/> |Specifies the site collection that contains the InfoPath 2016 form template and Central Administration .udcx files to export.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL, in the form http://server_name; or an instance of a valid **SPSite** object.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPFormsServicePipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------EXAMPLE--------------
  
```
Export-SPInfoPathAdministrationFiles -path d:\file.cab
```

This example saves all InfoPath 2016 form templates (.xsn files) and universal data connections (.udcx files) located on the SharePoint Central Administration Web site in a compressed cabinet file named  `file.cab`.
  
## See also

#### 

[Import-SPInfoPathAdministrationFiles](import-spinfopathadministrationfiles.md)

