---
title: "Set-SPAccessServicesDatabaseServer"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/20/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fe3917a4-9b8f-4bd2-b346-8350e3aad9d4

description: "Specifies whether or not a database in SQL Server is available."
---

# Set-SPAccessServicesDatabaseServer

Specifies whether or not a database in SQL Server is available.
  
```
Set-SPAccessServicesDatabaseServer -DatabaseServer <AccessServicesDatabaseServerPipeBind> -DatabaseServerGroup <AccessServicesDatabaseServerGroupPipeBind> -ServiceContext <SPServiceContextPipeBind> [-DatabaseServerCredentials <PSCredential>] [-DatabaseServerName <String>] <COMMON PARAMETERS>

```

## Example

```
$context = [Microsoft.SharePoint.SPServiceContext]::GetContext($app.ServiceApplicationProxyGroup, [Microsoft.SharePoint.SPSiteSubscriptionIdentifier]::Default)
```

```
$sqlServerName = "SQLServer2012AppDbServer"
```

```
$serverGroupName = 'DEFAULT'
```

```
$newdbserver = New-SPAccessServicesDatabaseServer -ServiceContext $context -DatabaseServerName $sqlServerName -DatabaseServerGroup $serverGroupName -AvailableForCreate $true
```

```
Set-SPAccessServicesDatabaseServer $context -DatabaseServer $newdbserver -DatabaseServerGroup "DEFAULT" -AvailableForCreate $false
```

This example sets the Access Services database server by using the  `$context` and  `$newdbserver` variables. 
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
Use the **Set-SPAccessServicesDatabaseServer** cmdlet to specify whether or not a database in SQL Server is available for creation of new Access Services applications. 
  
If you use the **Set-SPAccessServicesDatabaseServer** cmdlet in hosted mode, you receive the following error message: 
  
This operation is not supported when Access Services is running in hosted mode.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AvailableForCreate_ <br/> |Required  <br/> |System.Boolean  <br/> |Specifies whether the new server should be available for new database creation.  <br/> The default value is **True**. Setting the value to **True** will set all other servers in the list to **False**.  <br/> |
| _DatabaseServer_ <br/> |Required  <br/> |Microsoft.Office.Access.Services.PowerShell.AccessServicesDatabaseServerPipeBind  <br/> |Specifies the ServerID of the server running SQL Server to update.  <br/> |
| _DatabaseServerGroup_ <br/> |Required  <br/> |Microsoft.Office.Access.Services.PowerShell.AccessServicesDatabaseServerGroupPipeBind  <br/> |Specifies the Access Services database server group to be set.  <br/> |
| _Encrypt_ <br/> |Required  <br/> |System.Boolean  <br/> |Specifies all connections to the database server will use Secure Sockets Layer (SSL) if the database supports it.  <br/> |
| _Failover_ <br/> |Required  <br/> |System.Boolean  <br/> |PARAMVALUE: $true | $false  <br/> |
| _ServiceContext_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context for the Access Services database server to be set.  <br/> |
| _State_ <br/> |Required  <br/> |Microsoft.Office.Access.Services.MossHost.DatabaseServerStates  <br/> | Specifies the various states that can be applied on the server. This is the same as MossHost.DatabaseServerState enumeration.  <br/>  The valid values are:  <br/>  Active  <br/>  Locked  <br/>  Reserved  <br/> |
| _StateOwner_ <br/> |Required  <br/> |Microsoft.Office.Access.Services.MossHost.ServerStateOwner  <br/> | Specifies the owner responsible for setting the state. This is the same as MossHost.ServerStateOwner enumeration.  <br/>  By default the value is **NoOwner**, but the server can be put in specific state by various features.  <br/>  The valid values are:  <br/>  NoOwner  <br/>  TenantMove  <br/> |
| _TrustServerCertificate_ <br/> |Required  <br/> |System.Boolean  <br/> |Specifies whether SSL certificates are always trusted when using encrypted connections.  <br/> The valid values are $true or $false.  <br/> |
| _UserDomain_ <br/> |Required  <br/> |System.String  <br/> |Specifies the User Domain for login usernames that are used for OneBox for Azure SQL.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseServerCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the Credential object for the database user. Use this parameter if you use SQL Server Authentication. If no database credentials are provided, Windows authentication is used.  <br/> |
| _DatabaseServerName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the database server name.  <br/> |
| _Exclusive_ <br/> |Optional  <br/> |System.Boolean  <br/> |Enables the AvailableForCreate flag for this server and disables it for all other servers in the DatabaseServerGroup.  <br/> |
| _SecondaryDatabaseServerName_ <br/> |Optional  <br/> |System.String  <br/> |The name of the secondary database server.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Get-SPAccessServicesDatabaseServer](get-spaccessservicesdatabaseserver.md)
  
[Remove-SPAccessServicesDatabaseServer](remove-spaccessservicesdatabaseserver.md)
  
[New-SPAccessServicesDatabaseServer](new-spaccessservicesdatabaseserver.md)

