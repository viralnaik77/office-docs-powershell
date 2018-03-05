---
title: "Remove-SPAccessServicesDatabaseServer"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/20/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 25e20551-8be0-48f6-b094-8b5dd361e34b

description: "Removes the specified database server."
---

# Remove-SPAccessServicesDatabaseServer

Removes the specified database server.
  
```
Remove-SPAccessServicesDatabaseServer -DatabaseServer <AccessServicesDatabaseServerPipeBind> -DatabaseServerGroup <AccessServicesDatabaseServerGroupPipeBind> -ServiceContext <SPServiceContextPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------------EXAMPLE--------
  
```
$serverGroupName = 'DEFAULT'
```

```
$context = [Microsoft.SharePoint.SPServiceContext]::GetContext($app.ServiceApplicationProxyGroup, [Microsoft.SharePoint.SPSiteSubscriptionIdentifier]::Default)
```

```
$sqlServerName = "SQLServer2012AppDbServer"
```

```
$newdbserver = New-SPAccessServicesDatabaseServer -ServiceContext $context -DatabaseServerName $sqlServerName -DatabaseServerGroup $serverGroupName -AvailableForCreate $true
```

```
Remove-SPAccessServicesDatabaseServer -ServiceContext $context -DatabaseServer $newdbserver -DatabaseServerGroup "DEFAULT"
```

This example removes all Access Services database servers from the default group.
  
## Detailed Description

Use the **Remove-SPAccessServicesDatabaseServer** cmdlet to remove the target Access Services database server by using the **DatabaseServerGroup** and **ServiceContext** parameters. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _DatabaseServer_ <br/> |Required  <br/> |Microsoft.Office.Access.Services.PowerShell.AccessServicesDatabaseServerPipeBind  <br/> |Specifies the database server to be deleted.  <br/> |
| _DatabaseServerGroup_ <br/> |Required  <br/> |Microsoft.Office.Access.Services.PowerShell.AccessServicesDatabaseServerGroupPipeBind  <br/> |Specifies the Access Services database server group to remove.  <br/> |
| _ServiceContext_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context to remove the Access Services database server.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Force_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Force removing the database server.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Get-SPAccessServicesDatabaseServer](get-spaccessservicesdatabaseserver.md)
  
[New-SPAccessServicesDatabaseServer](new-spaccessservicesdatabaseserver.md)
  
[Set-SPAccessServicesDatabaseServer](set-spaccessservicesdatabaseserver.md)

