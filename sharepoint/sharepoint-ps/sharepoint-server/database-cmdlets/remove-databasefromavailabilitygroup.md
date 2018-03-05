---
title: "Remove-DatabaseFromAvailabilityGroup"
ms.author: kirks
author: Techwriter40
ms.date: 2/10/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 38994ce7-7fc3-499b-8067-28ddcc4fade2

description: "Removes one or more SharePoint databases from an availability group in SQL Server."
---

# Remove-DatabaseFromAvailabilityGroup

Removes one or more SharePoint databases from an availability group in SQL Server.
  
```
Remove-DatabaseFromAvailabilityGroup -DatabaseName <String> <COMMON PARAMETERS>

```

## Example

--------------EXAMPLE----------- 
  
```
Remove-DatabaseFromAvailabilityGroup -AGName MyAvailabilityGroup -DatabaseName WSS_Content 
```

This example removes the availability group named "MyAvailabilityGroup" from the WSS_Content database.
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AGName_ <br/> |Required  <br/> |System.String  <br/> |The name of the availability group from which the databases are being added.  <br/> |
| _DatabaseName_ <br/> |Required  <br/> |System.String  <br/> |The name of the database to be removed from the availability group.  <br/> > [!NOTE]> This parameter should not be used in conjunction with the **ProcessAllDatabases** parameter.           |
| _ProcessAllDatabases_ <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Removes all databases from the current SharePoint farm into the availability group.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Force_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forces a remove from the group.  <br/> |
| _KeepSecondaryData_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that copies of the databases on the replicas in the availability group will not be deleted. Otherwise, those database copies will be dropped.  <br/> |
   
## See also

#### 

[Add-DatabaseToAvailabilityGroup](add-databasetoavailabilitygroup.md)
  
[Get-AvailabilityGroupStatus](get-availabilitygroupstatus.md)

