---
title: "Suspend-SPStateServiceDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 451f6734-2647-4d76-b85e-330729f31e5b

description: "Pauses a state database and thus prevents new rows of data from being added to a database."
---

# Suspend-SPStateServiceDatabase

Pauses a state database and thus prevents new rows of data from being added to a database.
  
```
Suspend-SPStateServiceDatabase [-Identity] <SPStateDatabasePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Suspend-SPStateServiceDatabase** cmdlet pauses a state database. This cmdlet updates the state database object that is specified in the **Identity** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Administration.SPStateDatabasePipeBind  <br/> |Specifies the state database to pause.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a state database (for example, StateSvcDB1); or an instance of a valid **SPStateServiceDatabase** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Administration.SPStateDatabasePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Suspend-SPStateServiceDatabase -Identity 9703f7e2-9521-47c3-bd92-80e3eeba391b
```

This example suspends a specified state service database.
  
## See also

#### 

[Dismount-SPStateServiceDatabase](dismount-spstateservicedatabase.md)
  
[Initialize-SPStateServiceDatabase](initialize-spstateservicedatabase.md)
  
[Mount-SPStateServiceDatabase](mount-spstateservicedatabase.md)
  
[New-SPStateServiceDatabase](new-spstateservicedatabase.md)
  
[Remove-SPStateServiceDatabase](remove-spstateservicedatabase.md)
  
[Resume-SPStateServiceDatabase](resume-spstateservicedatabase.md)
  
[Set-SPStateServiceDatabase](set-spstateservicedatabase.md)

