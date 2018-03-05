---
title: "Get-SPDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9802bf8-5216-4ade-b559-7ee25fcfa666

description: "Retrieves all properties of a database."
---

# Get-SPDatabase

Retrieves all properties of a database.
  
```
Get-SPDatabase [-Identity <SPDatabasePipeBind>] <COMMON PARAMETERS>

```

## Example

--------------------EXAMPLE---------------------
  
```
Get-SPDatabase -ServerInstance "ServerA\SharePoint"
```

This example gets all databases on a specific named SQL Server Express instance.
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
The **Get-SPDatabase** cmdlet displays all public properties of a database to the current window. If the **Identity** parameter is specified, only properties of that ID are displayed. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the database.  <br/> |
| _ServerInstance_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPDatabaseServiceInstancePipeBind  <br/> |Specifies the name of the SQL instance that contains the database in either the form "Server" for a default SQL instance or "Server\Instance" for a named SQL instance.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPDatabasePipeBind  <br/> |Specifies the name of the database to display public properties.  <br/> The type must be a valid GUID, in the form 1234-3456-567kg.  <br/> |
   
## See also

#### 

[Get-SPContentDatabase](get-spcontentdatabase.md)
  
[Set-SPContentDatabase](set-spcontentdatabase.md)
#### 

[New-SPContentDatabase](http://technet.microsoft.com/library/18cf18cd-8fb7-4561-be71-41c767f27b51.aspx)

