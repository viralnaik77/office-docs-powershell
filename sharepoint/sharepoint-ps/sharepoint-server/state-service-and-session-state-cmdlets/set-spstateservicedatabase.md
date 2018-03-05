---
title: "Set-SPStateServiceDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3ce7acf2-23f5-48cf-b4a7-f4244638dc05

description: "Updates properties of a state service database."
---

# Set-SPStateServiceDatabase

Updates properties of a state service database.
  
```
Set-SPStateServiceDatabase -Identity <SPStateDatabasePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DatabaseCredentials <PSCredential>] [-ServiceApplication <SPStateServiceApplicationPipeBind>] [-Weight <Int32>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------------EXAMPLE 1--------------
  
```
Set-SPStateServiceDatabase -Identity 9703f7e2-9521-47c3-bd92-80e3eeba391b -Weight 10
```

This example updates the database weight to the maximum ( `10`).
  
--------------EXAMPLE 2--------------
  
```
Set-SPStateServiceDatabase -Identity 9703f7e2-9521-47c3-bd92-80e3eeba391b -ServiceApplication "StateSvcApp1"
```

This example updates the associated service application for a state service database.
  
--------------EXAMPLE 3--------------
  
```
$cred = Get-Credential
```

```
Set-SPStateServiceDatabase -Identity "StateSvcDB1" -DatabaseCredentials $cred
```

This example updates the SQL Authentication credentials that are used for a given database.
  
## Detailed Description

The **Set-SPStateServiceDatabase** cmdlet manages the credentials that are used to communicate with the database, sets the weight of the database, or changes the state service application with which it is associated. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Administration.SPStateDatabasePipeBind  <br/> |Specifies the state service database to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a state database (for example, StateSvcDB1); or an instance of a valid **SPStateServiceDatabase** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the database credentials for SQL Authentication used to access the state service database. If this parameter is not specified, Windows authentication is used.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _ServiceApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Administration.SPStateServiceApplicationPipeBind  <br/> |Specifies the state service application to which to add the state database.  <br/> The type must be a valid name of a state service application (for example, StateServiceApp1); a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid **SPStateServiceApplication** object.  <br/> |
| _Weight_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the weight for the state database. The default value is **1**.  <br/> The type must be a valid integer in the range of 1 to 10.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Administration.SPStateDatabasePipeBind  <br/> ||
|**ServiceApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Administration.SPStateServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**Weight** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Dismount-SPStateServiceDatabase](dismount-spstateservicedatabase.md)
  
[Initialize-SPStateServiceDatabase](initialize-spstateservicedatabase.md)
  
[Mount-SPStateServiceDatabase](mount-spstateservicedatabase.md)
  
[New-SPStateServiceDatabase](new-spstateservicedatabase.md)
  
[Remove-SPStateServiceDatabase](remove-spstateservicedatabase.md)
  
[Resume-SPStateServiceDatabase](resume-spstateservicedatabase.md)
  
[Suspend-SPStateServiceDatabase](suspend-spstateservicedatabase.md)

