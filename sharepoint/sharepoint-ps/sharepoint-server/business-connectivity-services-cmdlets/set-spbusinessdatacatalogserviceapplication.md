---
title: "Set-SPBusinessDataCatalogServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/20/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eb16e01e-25ee-42e1-9df2-a9a097a2bb8a

description: "Sets global properties for a Business Data Connectivity service application in the farm."
---

# Set-SPBusinessDataCatalogServiceApplication

Sets global properties for a Business Data Connectivity service application in the farm.
  
```
Set-SPBusinessDataCatalogServiceApplication -Identity <SPServiceApplicationPipeBind> [-ApplicationPool <SPIisWebServiceApplicationPool>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DatabaseCredentials <PSCredential>] [-DatabaseName <String>] [-DatabasePassword <SecureString>] [-DatabaseServer <String>] [-DatabaseUsername <String>] [-FailoverDatabaseServer <String>] [-Name <String>] [-Sharing <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPBusinessDataCatalogServiceApplication** cmdlet sets global properties for a Business Data Connectivity service application in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationPool** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPIisWebServiceApplicationPool  <br/> |Specifies the IIS application pool to use for the new Business Data Connectivity service application.  <br/> |
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the **PSCredential** object that contains the user name and password to be used for database SQL Server Authentication.  <br/> The type must be a valid **PSCredential** object.  <br/> |
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the Business Data Connectivity database.  <br/> The type must be a valid name of a SQL Server database; for example, UsageLogDB1.  <br/> |
|**DatabasePassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the password for the user specified in **DatabaseUserName**. Use this parameter only if SQL Server Authentication is used to access the Business Data Connectivity database.  <br/> The type must be a valid password.  <br/> |
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the Business Data Connectivity database.  <br/> The type must be a valid name of a SQL Server database; for example, UsageLogDB1.  <br/> |
|**DatabaseUsername** <br/> |Optional  <br/> |System.String  <br/> |Specifies the user name to use for connecting to the catalog database. Use this parameter only if SQL Server Authentication is used to access the Business Data Connectivity database.  <br/> The type must be a valid user name; for example, UserName1.  <br/> |
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the failover database server.  <br/> The type must be a valid SQL Server host name; for example, SQLServerHost1.  <br/> |
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> |Specifies the Business Data Connectivity service application associated with the new proxy.  <br/> |
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies a display name for the new Business Data Connectivity service application proxy.  <br/> |
|**Sharing** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the Business Data Connectivity service application is published and shared across the farm.  <br/> |
|**AssignmentColletion** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**ApplicationPool** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPIisWebServiceApplicationPool  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabasePassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseUsername** <br/> |Optional  <br/> |System.String  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**Sharing** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Set-SPBusinessDataCatalogServiceApplication -Identity $serviceApplication -FailoverDatabaseServer "CONTOSO\Backup"
```

This example sets the failover database server to  `CONTOSO\Backup` for the given service application. 
  
## See also

#### 

[New-SPBusinessDataCatalogServiceApplication](new-spbusinessdatacatalogserviceapplication.md)
  
[New-SPBusinessDataCatalogServiceApplicationProxy](new-spbusinessdatacatalogserviceapplicationproxy.md)

