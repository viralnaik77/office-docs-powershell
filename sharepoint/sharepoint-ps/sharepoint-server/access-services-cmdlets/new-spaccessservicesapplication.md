---
title: "New-SPAccessServicesApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/20/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2866e9dd-61df-4e45-a0ce-23d9ff0583cc

description: "Creates a new instance of an Access Services application in SharePoint Server 2016."
---

# New-SPAccessServicesApplication

Creates a new instance of an Access Services application in SharePoint Server 2016.
  
```
New-SPAccessServicesApplication -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> [-CacheTimeout <Int32>] [-Default <SwitchParameter>] [-Hosted <$true | $false>] [-Name <String>] [-PrivateBytesMax <Int32>] [-QueryTimeout <Int32>] [-RecoveryPointObjective <Int32>] [-RequestDurationMax <Int32>] [-SessionsPerAnonymousUserMax <Int32>] [-SessionsPerUserMax <Int32>] <COMMON PARAMETERS>

```

## Example

-----------EXAMPLE--------
  
```
$serviceAppName = "Access Services"
```

```
$onPremAppPool = "on-prem-pool"
```

```
$sqlServerName = "SQLServer2012AppDbServer"
```

```
$ApplicationPool = Get-SPServiceApplicationPool -Identity $onPremAppPool
```

```
New-SPAccessServicesApplication -Name $serviceAppName -ApplicationPool $ApplicationPool -Default -DatabaseServer $sqlServerName
```

This example creates a new Access Services services application named  `Access Services`
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
The **New-SPAccessServiceApplication** cmdlet creates a new instance of an Access Services application in SharePoint Server 2016. After you create a new Access Services application, use the **Set-SPAccessServiceApplication** cmdlet to modify its global settings. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ApplicationPool_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the existing Internet Information Services (IIS) application pool to run the Web service in for the new Access Services application.  <br/> The value must be a valid instance of a **SPIisWebServiceApplicationPool** object.  <br/> |
| _DatabaseServer_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the Microsoft SQL database server.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CacheTimeout_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of seconds that a data cache will remain active on Access Services with no user activity. Valid values include: **-1**, cache never times out; 1 to 2073600, cache remains active from 1 second to 24 days.  <br/> The value must be the integers -1, or an integer in the range of 1 to 2073600 (24 days). The default value is **300**.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseServerCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the **PSCredential** object that contains the user name and password to be used for database SQL authentication. If no database credentials are provided, Windows authentication is used.  <br/> |
| _Default_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the service application is associated with web applications by adding this service application's proxy to the farm's default proxy list.  <br/> |
| _Encrypt_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether the initial connection to the server must be encrypted.  <br/> |
| _Hosted_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that the Access Services application is used in a hosted environment that includes management of logical servers.  <br/> The default value is false.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the display name of the Access Services application to create. The name can contain a maximum of 128 characters and can contain the comma (,), equal sign (=), or colon (:) characters if they are enclosed in quotation marks.  <br/> The type must be a valid name of an Access Services application; for example, **AccessSrvApp1**.  <br/> |
| _PrivateBytesMax_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum private bytes in megabytes (MB) that can be used by Access Services. When set to -1, Access Services defaults to 75 percent of physical memory on the server. Valid values are -1 (no limit), and from 1 to any positive integer.The default value is - **1**.  <br/> |
| _QueryTimeout_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of seconds for a query to execute.  <br/> |
| _RecoveryPointObjective_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum amount of time in minutes by which the replica can fall behind the primary before the primary is read-only when geo-replication is used.  <br/> |
| _RequestDurationMax_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of seconds that a request to perform an operation can use before the request times out. Valid values include: -1, no limit, 1 to 2073600, cache remains active 1 second to 24 days. The default value is **30**.  <br/> The value must be the integer -1, or an integer in the range of 1 to 2073600 (24 days)  <br/> |
| _SessionsPerAnonymousUserMax_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of sessions allowed per user. If this maximum is exceeded, the oldest session is deleted when a new session is started. Valid values include: -1, no limit, and 1 to any positive integer. The default value is **10**.  <br/> The value must be the integer -1, or an integer in the range of 1 to MaxInt.  <br/> |
| _SessionsPerUserMax_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of sessions allowed per user. If this maximum is exceeded, the oldest session is deleted when a new session is started. Valid values include: -1, no limit, and 1 to any positive integer. The default value is **10**.  <br/> The value must be the integer -1, or an integer in the range of 1 to MaxInt.  <br/> |
| _TrustServerCertificate_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies if SSL certificates are always trusted when using encrypted connections.  <br/> The default value is false.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**DatabaseServer** <br/> |Required  <br/> |System.String  <br/> ||
|**Default** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CacheTimeout** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseServerCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**Encrypt** <br/> |Optional  <br/> |System.Boolean  <br/> ||
|**Hosted** <br/> |Optional  <br/> |System.Boolean  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**PrivateBytesMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**QueryTimeout** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**RequestDurationMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**SessionsPerAnonymousUserMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**SessionsPerUserMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPAccessServicesApplication](get-spaccessservicesapplication.md)
  
[Set-SPAccessServicesApplication](set-spaccessservicesapplication.md)

