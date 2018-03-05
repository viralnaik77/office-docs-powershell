---
title: "New-SPUsageApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6425f876-81a4-4005-9e0a-1376856d4934

description: "Creates a new usage application."
---

# New-SPUsageApplication

Creates a new usage application.
  
```
New-SPUsageApplication [[-Name] <String>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DatabaseName <String>] [-DatabasePassword <SecureString>] [-DatabaseServer <String>] [-DatabaseUsername <String>] [-FailoverDatabaseServer <String>] [-UsageService <SPUsageServicePipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **New-SPUsageApplication** cmdlet creates a new usage application in the local farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the friendly name of the new usage application.  <br/> The type must be a valid name of a usage application; for example, UsageApplication1.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the logging database. If the logging database does not exist, a logging database is automatically created.  <br/> The type must be a valid name of a SQL Server database; for example, UsageLogDB1.  <br/> |
|**DatabasePassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the password for the user specified in **DatabaseUserName**. Use this parameter only if SQL Server Authentication is used to access the logging database.  <br/> The type must be a valid password.  <br/> |
|**DatabaseServer** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServerPipeBind  <br/> |Specifies the **SPServer** object where the logging database is created.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; the IP address of a server computer, in the form 208.77.188.166; a valid name of a SQL Server host service (for example, SQLServerHost1); or an instance of a valid **SPServer** object.  <br/> |
|**DatabaseUsername** <br/> |Optional  <br/> |System.String  <br/> |Specifies the user name to use for connecting to the logging database. Use this parameter only if SQL Server Authentication is used to access the logging database.  <br/> The type must be a valid user name; for example, UserName1.  <br/> |
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host SQL Server instance for the failover database server.  <br/> The type must be a valid SQL Server instance name; for example, SQLServerHost1.  <br/> |
|**UsageService** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUsageServicePipeBind  <br/> |Filters to return the usage application with the specified parent **SPUsageService** object.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a usage service (for example, UsageService1); or an instance of a valid **SPUsageService** object.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabasePassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseUsername** <br/> |Optional  <br/> |System.String  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**UsageService** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUsageServicePipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-------------------EXAMPLE------------------------- 
  
```
New-SPUsageApplication -Name "Usage Application For Farm ABC"
```

This example creates a new usage application for the specified name.
  

