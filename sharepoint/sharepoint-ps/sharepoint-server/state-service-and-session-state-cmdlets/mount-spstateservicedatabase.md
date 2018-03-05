---
title: "Mount-SPStateServiceDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd559347-c8f9-4ecf-9fbc-17821ae0afc4

description: "Attaches an existing state service database to the farm."
---

# Mount-SPStateServiceDatabase

Attaches an existing state service database to the farm.
  
```
Mount-SPStateServiceDatabase -Name <String> [-AssignmentCollection <SPAssignmentCollection>] [-DatabaseCredentials <PSCredential>] [-DatabaseServer <String>] [-ServiceApplication <SPStateServiceApplicationPipeBind>] [-Weight <Int32>]

```

## Example

--------------EXAMPLE 1-----------------
  
```
Mount-SPStateServiceDatabase -Name "statedata1" -DatabaseServer "localhost"
```

This example associates a SharePoint Server 2016 farm with a SQL Server database.
  
This example is used in least privilege scenarios when an administrator cannot create databases in SQL. The database must already exist and be empty. The database cannot be used until the **Initialize-SPStateServiceDatabase** cmdlet is run, so errors could occur with this example. 
  
--------------EXAMPLE 2-----------------
  
```
Mount-SPStateServiceDatabase -Name "statedata1" -DatabaseServer "localhost" -ServiceApplication "ServiceApp1" -Weight 10 | Initialize-SPStateServiceDatabase
```

This example associates a SharePoint Server 2016 farm with a SQL Server database, at the same time that it also associates the database with a service application and gives a weight of  `10`. The result is immediately piped to the **Initialize-SPStateServiceDatabase** cmdlet so that the database can be used. 
  
## Detailed Description

The **Mount-SPStateServiceDatabase** cmdlet attaches an existing state service database to the farm. If the session state database schema is not installed in the state service database, use the **Initialize-SPStateServiceDatabase** cmdlet to install the schema after the state service database has been mounted. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the database name that is created in the SQL Server database.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _DatabaseCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the database credentials for SQL Authentication used to access the state service database. If this parameter is not specified, Windows authentication is used.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the state service database.  <br/> The type must be a valid SQL Server host name; for example, SQLServerHost1.  <br/> |
| _ServiceApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Administration.SPStateServiceApplicationPipeBind  <br/> |Specifies the state service application to which to add the state database.  <br/> The type must be a valid name of a state service application (for example, StateServiceApp1); a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid **SPStateServiceApplication** object.  <br/> |
| _Weight_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the weight for the state database used to load balance the allocation of new data. The default value is **1**.  <br/> The type must be a valid integer in the range of 1 to 10.  <br/> |
   
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
  
[New-SPStateServiceDatabase](new-spstateservicedatabase.md)
  
[Remove-SPStateServiceDatabase](remove-spstateservicedatabase.md)
  
[Resume-SPStateServiceDatabase](resume-spstateservicedatabase.md)
  
[Set-SPStateServiceDatabase](set-spstateservicedatabase.md)
  
[Suspend-SPStateServiceDatabase](suspend-spstateservicedatabase.md)

