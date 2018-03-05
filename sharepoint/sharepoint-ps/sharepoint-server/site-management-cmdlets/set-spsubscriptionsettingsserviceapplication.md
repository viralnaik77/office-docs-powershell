---
title: "Set-SPSubscriptionSettingsServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 462e367f-47bb-4eca-89fa-e7c1d3ba9126

description: "Sets properties of a subscription settings service application."
---

# Set-SPSubscriptionSettingsServiceApplication

Sets properties of a subscription settings service application.
  
```
Set-SPSubscriptionSettingsServiceApplication [-Identity] <SPServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DatabaseCredentials <PSCredential>] [-DatabaseName <String>] [-DatabaseServer <String>] [-FailoverDatabaseServer <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Set-SPSubscriptionSettingsServiceApplication** cmdlet to set properties on a subscription settings service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> |Specifies the settings service application to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a subscription settings service application (for example, SubscriptionSettingsApp1); or an instance of a valid **SPSubscriptionSettingsServiceApplication** object.  <br/> |
|**ApplicationPool** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the Internet Information Services (IIS) application pool to use for the new subscription settings application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an application pool (for example, AppPoolName1); or an instance of a valid **IISWebServiceApplicationPool** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the **PSCredential** object that contains the user name and password to be used for database SQL Server Authentication.  <br/> The type must be a valid **PSCredential** object.  <br/> |
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the subscription settings database.  <br/> The type must be a valid name of a SQL Server database; for example, SubscriptionSettingsAppDB1.  <br/> |
|**DatabaseServer** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServerPipeBind  <br/> |Specifies the name of the host SQL Server instance for the database specified in **DatabaseName** parameter.  <br/> The type must be a valid SQL Server instance name; for example, SQLServerHost1.  <br/> |
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host SQL Server instance for the failover database server.  <br/> The type must be a valid SQL Server instance name; for example, SQLServerHost1.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------------EXAMPLE--------------------------
  
```
$applicationPool = GetServiceApplicationPool SettingsApplicationPool
```

```
Get-SPServiceApplication -Name SettingsServiceApp | Set-SPSubscriptionSettingsServiceApplication -ApplicationPool $applicationPool
```

This example changes the application pool of the subscription settings service application. This command assumes that a subscription settings service application named  `SettingsServiceApp` exists and that an application pool named  `SettingsApplicationPool` exists 
  
## See also

#### 

[New-SPSubscriptionSettingsServiceApplication](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/service-application-cmdlets/new-spsubscriptionsettingsserviceapplication.md)
  
[New-SPSubscriptionSettingsServiceApplicationProxy](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/service-application-cmdlets/new-spsubscriptionsettingsserviceapplicationproxy.md)

