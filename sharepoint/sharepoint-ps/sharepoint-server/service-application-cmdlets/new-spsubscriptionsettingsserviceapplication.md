---
title: "New-SPSubscriptionSettingsServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0056290-df8b-4167-9a11-59cbb619e194

description: "Creates a new subscription settings service application."
---

# New-SPSubscriptionSettingsServiceApplication

Creates a new subscription settings service application.
  
```
New-SPSubscriptionSettingsServiceApplication -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DatabaseCredentials <PSCredential>] [-DatabaseName <String>] [-DatabaseServer <String>] [-DeferUpgradeActions <SwitchParameter>] [-FailoverDatabaseServer <String>] [-Name <String>] [-WhatIf [<SwitchParameter>]]

```

## Example

-------------EXAMPLE--------------- 
  
```
$AppPool = New-SPServiceApplicationPool -Name SettingsServiceAppPool -Account (Get-SPManagedAccount DOMAIN\jdoe)
```

```
$App = New-SPSubscriptionSettingsServiceApplication -ApplicationPool $appPool -Name SettingsServiceApp -DatabaseName SettingsServiceDB
```

```
$proxy = New-SPSubscriptionSettingsServiceApplicationProxy -ServiceApplication $App
```

```
Get-SPServiceInstance | where{$_.TypeName -eq "Microsoft SharePoint Foundation Subscription Settings Service"} | Start-SPServiceInstance
```

This example creates an application pool, a new subscription settings service application, a subscription settings service application proxy, and starts the service instance on the local machine. This example assumes that a managed account for  `DOMAIN\jdoe` already exists. 
  
## Detailed Description

Use the **New-SPSubscriptionSettingsServiceApplication** cmdlet to create a subscription settings service application that can be used to store settings that are shared across all site collections in a single site subscription. This cmdlet is used only in an environment where site subscriptions are used to delegate administration or partition services that are used for storing settings that are shared across all site collections in a single site subscription. This cmdlet is used only in an environment where site subscriptions are used to delegate administration or partition services. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ApplicationPool_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the IIS application pool to use for the new subscription settings application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an application pool (for example, AppPoolName1); or an instance of a valid **IISWebServiceApplicationPool** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the **PSCredential** object that contains the user name and password to be used for database SQL Server Authentication.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _DatabaseName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the subscription settings database.  <br/> If not provided, one will be generated.  <br/> The type must be a valid name of a SQL Server database; for example, SubscriptionSettingsApp1.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host SQL Server instance for the database specified in the **DatabaseName** parameter. If not provided, the default database server will be used  <br/> The type must be a valid SQL Server instance name; for example, SQLServerHost1.  <br/> The type must be a valid name of a SQL Server database; for example, SubscriptionSettingsApp1.  <br/> |
| _DeferUpgradeActions_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to defer the upgrade process.  <br/> |
| _FailoverDatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host SQL Server instance for the failover database server.  <br/> The type must be a valid SQL Server instance name; for example, SQLServerHost1.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the friendly name of the new subscription settings service.  <br/> The type must be a valid name of a subscription settings service application; for example, SubscriptionSettingsApp1.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Set-SPSubscriptionSettingsServiceApplication](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/set-spsubscriptionsettingsserviceapplication.md)
  
[New-SPSubscriptionSettingsServiceApplicationProxy](new-spsubscriptionsettingsserviceapplicationproxy.md)

