---
title: "New-SPStateServiceDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 221e439c-c501-4d4c-9d8a-171a01e67e25

description: "Creates and provisions a new state service database, and installs the state database schema into it."
---

# New-SPStateServiceDatabase

Creates and provisions a new state service database, and installs the state database schema into it.
  
```
New-SPStateServiceDatabase -Name <String> [-AssignmentCollection <SPAssignmentCollection>] [-DatabaseCredentials <PSCredential>] [-DatabaseServer <String>] [-ServiceApplication <SPStateServiceApplicationPipeBind>] [-Weight <Int32>]

```

## Example

--------------EXAMPLE 1-----------------
  
```
Get-SPStateServiceApplication -name "State Service Application 1" | New-SPStateServiceDatabase -Name "statedata1" -DatabaseServer "localhost"
```

This example creates a new state service database by using Windows authentication, and associates it with the provided service application. 
  
--------------EXAMPLE 2-----------------
  
```
$cred = Get-Credential
```

```
Get-SPStateServiceApplication -name "State Service Application 1" | New-SPStateServiceDatabase -Name "statedata1" -DatabaseServer "localhost" -DatabaseCredentials $cred
```

This example creates a new state service database, a new state service application associated with the database and a new state service application proxy associated with the state service application proxy.
  
This example configures all the objects required to have State Service operational on a farm.
  
## Detailed Description

The **New-SPStateServiceDatabase** cmdlet creates and a new state service database. This cmdlet installs the session state database schema in the state service database. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name for the state service database that is stored in SQL Server.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _DatabaseCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the database credentials for SQL Authentication used to access the state service database. If this parameter is not specified, Windows authentication is used.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the state service database.  <br/> The type must be a valid SQL Server host name; for example, SQLServerHost1.  <br/> |
| _ServiceApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Administration.SPStateServiceApplicationPipeBind  <br/> |Specifies the state service application to add the state database to.  <br/> The type must be a valid name of a state service application (for example, StateServiceApp1); a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid **SPStateServiceApplication** object.  <br/> |
| _Weight_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the weight for the state database. The default value is **1**.  <br/> This parameter is used when new rows of data are allocated among the collection of databases that are associated with a service application  <br/> The type must be a valid integer in the range of 1 to 10.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**ServiceApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Administration.SPStateServiceApplicationPipeBind  <br/> ||
|**Weight** <br/> |Optional  <br/> |System.Nullable  <br/> ||
   
## See also

#### 

[Dismount-SPStateServiceDatabase](dismount-spstateservicedatabase.md)
  
[Initialize-SPStateServiceDatabase](initialize-spstateservicedatabase.md)
  
[Mount-SPStateServiceDatabase](mount-spstateservicedatabase.md)
  
[Remove-SPStateServiceDatabase](remove-spstateservicedatabase.md)
  
[Resume-SPStateServiceDatabase](resume-spstateservicedatabase.md)
  
[Set-SPStateServiceDatabase](set-spstateservicedatabase.md)
  
[Suspend-SPStateServiceDatabase](suspend-spstateservicedatabase.md)

