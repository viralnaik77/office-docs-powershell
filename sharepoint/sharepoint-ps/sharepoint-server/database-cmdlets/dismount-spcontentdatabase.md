---
title: "Dismount-SPContentDatabase"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89eea901-8d3f-4d4d-9638-941a1cafe259

description: "Detaches a content database from its currently associated Web application."
---

# Dismount-SPContentDatabase

Detaches a content database from its currently associated Web application.
  
```
Dismount-SPContentDatabase [-Identity] <SPContentDatabasePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Dismount-SPContentDatabase** cmdlet to detatch the given content database from its currently associated Web application. This cmdlet will not delete the content database. Use the **Remove-SPContentDatabase** cmdlet to delete a content database. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the content database to detach.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint content database (for example, SPContentDB1); or an instance of a valid **SPContentDatabase** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------EXAMPLE 1------------
  
```
Dismount-SPContentDatabase 12345678-90ab-cdef-1234-567890abcdef
```

This example detaches the content database with the GUID  `12345678-90ab-cdef-1234-567890abcdef` from its current parent Web application. 
  
--------------EXAMPLE 2------------
  
```
Get-SPContentDatabase -WebApplication http://sitename | Dismount-SPContentDatabase -WhatIf
```

This example detaches all content databases from the Web application on port 80 of the local machine. Remove the  `WhatIf` parameter to perform the operation. 
  
## See also

#### 

[Get-SPContentDatabase](get-spcontentdatabase.md)
  
[Set-SPContentDatabase](set-spcontentdatabase.md)
  
[Mount-SPContentDatabase](mount-spcontentdatabase.md)
  
[Test-SPContentDatabase](test-spcontentdatabase.md)
#### 

[New-SPContentDatabase](http://technet.microsoft.com/library/18cf18cd-8fb7-4561-be71-41c767f27b51.aspx)
  
[Remove-SPContentDatabase](http://technet.microsoft.com/library/e8c337b6-37af-4fdd-8469-a32f4d45c040.aspx)

