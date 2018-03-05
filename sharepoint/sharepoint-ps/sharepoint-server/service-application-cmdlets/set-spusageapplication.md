---
title: "Set-SPUsageApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/8/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4b918524-5af9-4265-9dcc-470f70fbaaba

description: "Sets properties of a usage application."
---

# Set-SPUsageApplication

Sets properties of a usage application.
  
```
Set-SPUsageApplication [-Identity] <SPUsageApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DatabaseName <String>] [-DatabasePassword <SecureString>] [-DatabaseServer <String>] [-DatabaseUsername <String>] [-EnableLogging <SwitchParameter>] [-FailoverDatabaseServer <String>] [-UsageService <SPUsageServicePipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPUsageApplication** cmdlet sets properties of a usage application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUsageApplicationPipeBind  <br/> |Specifies the usage application to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid name of a usage application (for example; UsageApp1); or an instance of a valid **SPServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the logging database.  <br/> The type must be a valid name of a SQL Server database; for example, UsageLogDB1.  <br/> If the logging database does not exist, a logging database will be automatically created.  <br/> |
|**DatabasePassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the password for the user specified in **DatabaseUserName**. Use this parameter only if SQL Server Authentication is used to access the logging database.  <br/> The type must be a valid password.  <br/> |
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the database specified in **DatabaseName**.  <br/> The type must be a valid SQL Server host name; for example, SQLServerHost1.  <br/> |
|**DatabaseUsername** <br/> |Optional  <br/> |System.String  <br/> |Specifies the user name to use for connecting to the logging database. Use this parameter only if SQL Server Authentication is used to access the logging database.  <br/> The type must be a valid user name; for example, UserName1.  <br/> |
|**EnableLogging** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that this usage application collects usage data.  <br/> |
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> |Specifies the database server for failover.  <br/> |
|**UsageService** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUsageServicePipeBind  <br/> |Specifies the **SPUsageService** object that is the parent of the usage application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a usage service (for example, UsageService1); or an instance of a valid **SPUsageService** object.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUsageApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabasePassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseUsername** <br/> |Optional  <br/> |System.String  <br/> ||
|**EnableLogging** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**UsageService** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUsageServicePipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-------------------EXAMPLE----------------------
  
```
Set-SPUsageApplication -Identity "Usage and Health data collection" -DatabaseServer "Server Name" -DatabaseName "New Logging DB"
```

This example changes the database server and database name used by the usage logging service to store logging data.
  
## See also

#### 

[Get-SPUsageApplication](get-spusageapplication.md)
  
[New-SPUsageApplication](new-spusageapplication.md)
  
[Remove-SPUsageApplication](remove-spusageapplication.md)

