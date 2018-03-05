---
title: "Add-DatabaseToAvailabilityGroup"
ms.author: kirks
author: Techwriter40
ms.date: 2/10/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: be80d41d-302c-4af9-b5fe-4172b2dabaf6

description: "Adds one or more databases from a SharePoint farm into an availability group in SQL Server."
---

# Add-DatabaseToAvailabilityGroup

Adds one or more databases from a SharePoint farm into an availability group in SQL Server.
  
```
Add-DatabaseToAvailabilityGroup -DatabaseName <String> <COMMON PARAMETERS>

```

## Example

--------------EXAMPLE----------- 
  
```
Add-DatabaseToAvailabilityGroup -AGName MyAvailabilityGroup -DatabaseName WSS_Content -FileShare \\backup\share\ 
```

This example adds an availability group named "MyAvailabilityGroup" to the WSS_Content Database
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AGName_ <br/> |Required  <br/> |System.String  <br/> |The name of the availability group from which the databases are being added.  <br/> |
| _DatabaseName_ <br/> |Required  <br/> |System.String  <br/> |The name of the database to be added to the availability group.  <br/> > [!NOTE]> This parameter should not be used in conjunction with the **ProcessAllDatabases** parameter.           |
| _ProcessAllDatabases_ <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Adds all databases from the current SharePoint farm into the availability group.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _FileShare_ <br/> |Optional  <br/> |System.String  <br/> |When a database is being added to the availability group, backup / restores are done from this location to propagate the database to all replicas.  <br/> |
   
## See also

#### 

[Get-AvailabilityGroupStatus](get-availabilitygroupstatus.md)
  
[Remove-DatabaseFromAvailabilityGroup](remove-databasefromavailabilitygroup.md)

