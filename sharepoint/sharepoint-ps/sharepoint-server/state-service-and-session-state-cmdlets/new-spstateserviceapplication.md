---
title: "New-SPStateServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9fe0940-2f01-45be-be77-905b8589e1a4

description: "Creates a new state service application."
---

# New-SPStateServiceApplication

Creates a new state service application.
  
```
New-SPStateServiceApplication [-Name] <String> [-AssignmentCollection <SPAssignmentCollection>] [-Database <SPStateDatabasePipeBind>]
```

## Detailed Description

The **New-SPStateServiceApplication** cmdlet creates a new state service application on the farm. A state service application is the container for state service databases. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the new service application.  <br/> The type must be a valid name of a service application; for example, StateSvcApp1.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Database** <br/> |Optional  <br/> |Microsoft.Office.Server.Administration.SPStateDatabasePipeBind  <br/> |Specifies the state service database that is associated with the new service application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a state database (for example, StateSvcDB1); or an instance of a valid **SPStateServiceDatabase** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Database** <br/> |Optional  <br/> |Microsoft.Office.Server.Administration.SPStateDatabasePipeBind  <br/> ||
   
## Example

--------------EXAMPLE 1-----------------
  
```
New-SPStateServiceApplication -Name "State Service Application 1"
```

This example creates a new state service application, named  `State Service Application 1`, on the farm.
  
State service applications are the container for databases. State service applications must have a proxy and a database created to be usable.
  
--------------EXAMPLE 2-----------------
  
```
New-SPStateServiceDatabase -Name "State Service Database" | New-SPStateServiceApplication -Name "StateServiceApp1" | New-SPStateServiceApplicationProxy -DefaultProxyGroup
```

This example creates a new state service database, a new state service application associated with the database and a new state service application proxy associated with the state service application proxy.
  
This example configures all the objects required to have State Service operational on a farm.
  
## See also

#### 

[Get-SPStateServiceApplication](get-spstateserviceapplication.md)
  
[Set-SPStateServiceApplication](set-spstateserviceapplication.md)

