---
title: "Enable-SPSessionStateService"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5852b315-3493-48f2-8d52-295f34ef695e

description: "Creates a session state database and turns on the session state service."
---

# Enable-SPSessionStateService

Creates a session state database and turns on the session state service.
  
```
Enable-SPSessionStateService -DatabaseName <String> [-DatabaseCredentials <PSCredential>] [-DatabaseServer <String>] <COMMON PARAMETERS>

```

## Example

--------------EXAMPLE 1-----------------
  
```
Enable-SPSessionStateService -DefaultProvision
```

This example enables a ASP.NET session state on a SharePoint Server 2016 farm that uses the defaults (database hosted on the configuration database SQL Server, using Windows authentication, 60-minute session time-out).
  
--------------EXAMPLE 2-----------------
  
```
Enable-SPSessionStateService -DatabaseName "SessionStateDatabase" -DatabaseServer "localhost" -SessionTimeout 120

```

This example enables a ASP.NET session state on a SharePoint Server 2016 farm that uses a custom database name, database server, session time-out of 120 minutes, and Windows credentials (due to the lack of a **DatabaseCredentials** parameter). 
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
The **Enable-SPSessionStateService** cmdlet creates a session state database, installs the ASP.NET session state schema, and updates the Web.config files on the farm to turn on the session state service. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _DatabaseName_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the database for the session state service.  <br/> The type must be a valid name of a SQL Server database; for example, SessionStateDB1.  <br/> |
| _DefaultProvision_ <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the default provisioning settings are used. The default provisioning settings are: Windows Authentication, Auto SQL Server (configuration database), and Auto Catalog Name.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the database credentials for SQL Authentication used to access the session state service database. If this parameter is not specified, Windows authentication is used.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the host SQL Server for the state service database.  <br/> The type must be a valid SQL Server host name; for example, SQLServerHost1.  <br/> |
| _SessionTimeout_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the time, in minutes, that a ASP .NET session state service will remain active with no user activity. The default value is **60**.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**DatabaseName** <br/> |Required  <br/> |System.String  <br/> ||
|**DefaultProvision** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**SessionTimeout** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Disable-SPSessionStateService](disable-spsessionstateservice.md)
  
[Get-SPSessionStateService](get-spsessionstateservice.md)
  
[Set-SPSessionStateService](set-spsessionstateservice.md)

