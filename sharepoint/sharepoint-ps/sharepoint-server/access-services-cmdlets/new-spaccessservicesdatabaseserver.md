---
title: "New-SPAccessServicesDatabaseServer"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/20/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf30f955-ff5a-4cd7-ac5b-f43f83e1a61a

description: "Adds a new SQL Server database to the list of servers."
---

# New-SPAccessServicesDatabaseServer

Adds a new SQL Server database to the list of servers.
  
```
New-SPAccessServicesDatabaseServer -DatabaseServerName <String> -ServiceContext <SPServiceContextPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-AvailableForCreate <$true | $false>] [-Confirm [<SwitchParameter>]] [-DatabaseServerCredentials <PSCredential>] [-DatabaseServerGroupName <String>] [-Encrypt <$true | $false>] [-Exclusive <$true | $false>] [-LoginType <ApplicationLogin | LocalDBApplicationLogin | ServerLogin | StorageAccountLogon | WindowsAzureServerLogin>] [-SecondaryDatabaseServerName <String>] [-ServerReferenceId <Guid>] [-State <Active | Locked | Reserved>] [-StateOwner <NoOwner | TenantMove>] [-TrustServerCertificate <$true | $false>] [-UserDomain <String>] [-ValidateServer <$true | $false>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------------EXAMPLE---------
  
```
$serverGroupName = 'DEFAULT'
```

```
$farm = Get-SPFarm;
```

```
$account = $($farm.DefaultServiceAccount.Name);
```

```
$serviceAppName = "Access Services"
```

```
$onPremAppPool = "on-prem-pool"
```

```
$identity = Get-SPServiceApplication -Name $serviceAppName
```

```
$acct = Get-SPManagedAccount -Identity $account
```

```
$ApplicationPool = Get-spserviceapplicationpool -Identity $onPremAppPool
```

```
if($ApplicationPool -eq $NULL)
{
    $ApplicationPool = new-spserviceapplicationpool -name $onPremAppPool -account $acct
}

```

```
New-SPAccessServicesApplication -Name $serviceAppName -ApplicationPool $ApplicationPool -Default
```

```
$ASapp = Get-SPAccessServicesApplication
```

```
$app = $Null
```

```
if ($ASapp.length -ne $Null) { $app = $ASapp[0] } else { $app = $ASapp }
```

```
$context = [Microsoft.SharePoint.SPServiceContext]::GetContext($app.ServiceApplicationProxyGroup, [Microsoft.SharePoint.SPSiteSubscriptionIdentifier]::Default)
```

```
$newdbserver = New-SPAccessServicesDatabaseServer -ServiceContext $context -DatabaseServerName $sqlServerName -DatabaseServerGroup $serverGroupName -AvailableForCreate $true
```

This example creates a new Access Services database server.
  
## Detailed Description

Use the **New-SPAccessServicesDatabaseServer** cmdlet to add a new SQL Server database to the list of servers for application databases. 
  
If you use the **New-SPAccessServicesDatabaseServer** cmdlet does in hosted mode, you receive the following error message: 
  
This operation is not supported when Access Services is running in hosted mode.
  
If the SQL Authentication method is selected for the database credentials, the method checks that the Secure Store service is running and is accessible to the service. If the Secure Store service is unable to connect, the following message is displayed:
  
Operation failed. Secure Store Service must be running and accessible to the service in order to use SQL Authentication credentials.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _DatabaseServerName_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the server running SQL Server that you choose to host the new Access Services application databases.  <br/> |
| _ServiceContext_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context to create the Access Services database server.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _AvailableForCreate_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether the new server should be available for new database creation.  <br/> The default value is **True**. Setting the value to **True** will set all other servers in the list to **False**.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseServerCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the Credential object for the database user. Use this parameter if you use SQL Server Authentication. If no database credentials are provided, Windows authentication is used.  <br/> |
| _DatabaseServerGroupName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the Access Services database server group name.  <br/> |
| _Encrypt_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies all connections to the database server will use Secure Sockets Layer (SSL) if the database supports it.  <br/> |
| _Exclusive_ <br/> |Optional  <br/> |System.Boolean  <br/> |Enables the AvailableForCreate flag for this server and disables it for all other servers in the DatabaseServerGroup.  <br/> |
| _LoginType_ <br/> |Optional  <br/> |Microsoft.Office.Access.Services.Host.LoginType  <br/> | Specifies the login type for the server.  <br/>  The valid values are:  <br/>  ApplicationLogin  <br/>  LocalDBApplicationLogin  <br/>  ServerLogin  <br/>  StorageAccountLogon  <br/>  WindowsAzureServerLogin  <br/> |
| _SecondaryDatabaseServerName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the secondary database server.  <br/> |
| _ServerReferenceId_ <br/> |Optional  <br/> |System.Guid  <br/> |A unique identifier for the database server. Used for maintaining continuity when restoring an existing content database to a different or new farm.  <br/> |
| _State_ <br/> |Optional  <br/> |Microsoft.Office.Access.Services.MossHost.DatabaseServerStates  <br/> | Specifies the various states that can be applied on the server. This is the same as MossHost.DatabaseServerState enumeration.  <br/>  The valid values are:  <br/>  Active  <br/>  Locked  <br/>  Reserved  <br/> |
| _StateOwner_ <br/> |Optional  <br/> |Microsoft.Office.Access.Services.MossHost.ServerStateOwner  <br/> | Specifies who owns the server.  <br/>  By default the value is **NoOwner**, but the server can be put in specific state by various features.  <br/>  The valid values are:  <br/>  NoOwner  <br/>  TenantMove  <br/> |
| _TrustServerCertificate_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether SSL certificates are always trusted when using encrypted connections.  <br/> The valid values are $true or $false.  <br/> |
| _UserDomain_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the User Domain for login usernames that are used for OneBox for Azure SQL.  <br/> |
| _ValidateServer_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether the server is validated before it is registered.  <br/> The valid values are $true or $false.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Get-SPAccessServicesDatabaseServer](get-spaccessservicesdatabaseserver.md)
  
[Remove-SPAccessServicesDatabaseServer](remove-spaccessservicesdatabaseserver.md)
  
[Set-SPAccessServicesDatabaseServer](set-spaccessservicesdatabaseserver.md)

