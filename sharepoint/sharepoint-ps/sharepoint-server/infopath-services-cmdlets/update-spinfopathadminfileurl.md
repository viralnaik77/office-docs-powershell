---
title: "Update-SPInfoPathAdminFileUrl"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0d3991ec-dfff-406b-b35d-d452a51dfc6c

description: "Updates InfoPath form templates (.xsn files) and universal data connections (.udcx files), including all .xsn files and .udcx files that were deployed by an administrator."
---

# Update-SPInfoPathAdminFileUrl

Updates InfoPath form templates (.xsn files) and universal data connections (.udcx files), including all .xsn files and .udcx files that were deployed by an administrator.
  
```
Update-SPInfoPathAdminFileUrl -Find <Uri> -Replace <Uri> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Scan <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Update-SPInfoPathAdminFileUrl** cmdlet updates data connections in administrator-approved InfoPath form templates (.xsn files) and universal data connections (.udcx files). This allows for InfoPath data connections that reference the current farm to be updated when content is migrated to a different farm URL. This cmdlet cannot update any references to URLs that exist in form template business logic (code). Typically, this cmdlet is used with the **Import-SPInfoPathAdministratorFiles** cmdlet. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Find** <br/> |Required  <br/> |System.Uri  <br/> |Specifies the URL to find.  <br/> The type must be a valid URL, in the form http://previous_server_name.  <br/> |
|**Replace** <br/> |Required  <br/> |System.Uri  <br/> |Specifies the URL to find.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Scan** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Run the tool and log the actions that can be taken. No content is changed as a result of the scan.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Find** <br/> |Required  <br/> |System.Uri  <br/> ||
|**Replace** <br/> |Required  <br/> |System.Uri  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Scan** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Get-SPWebApplication http://contoso2010 | Update-SPInfoPathAdminFileUrl-find "http://contoso2007" -replace "http://contoso2010"
```

This example updates data connections in administrator-approved InfoPath form templates and universal data connection files. Data connections that reference  `http://contoso 2007` are updated to reference  `http://contoso2010`.
  

