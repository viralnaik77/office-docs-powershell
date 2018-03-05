---
title: "New-SPBusinessDataCatalogServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/20/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d35cefac-c55e-41ac-b193-9557f052897a

description: "Creates a new Business Data Connectivity service application in the farm."
---

# New-SPBusinessDataCatalogServiceApplication

Creates a new Business Data Connectivity service application in the farm.
  
```
New-SPBusinessDataCatalogServiceApplication -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DatabaseCredentials <PSCredential>] [-DatabaseName <String>] [-DatabasePassword <SecureString>] [-DatabaseServer <String>] [-DatabaseUsername <String>] [-DeferUpgradeActions <SwitchParameter>] [-FailoverDatabaseServer <String>] [-Name <String>] [-PartitionMode <SwitchParameter>] [-Sharing <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
New-SPBusinessDataCatalogServiceApplication -ApplicationPool "SharePoint Web Services Default" -DatabaseName "ContosoBdcDB" -DatabaseServer "CONTOSO\SharePoint" -Name "ContosoServiceApp"
```

This example creates a Business Data Connectivity service application named  `ContosoServiceApp`. In this process it uses the  `SharePoint Web Services Default` application pool and creates a database named  `ContosoBdcDB`.
  
## Detailed Description

The **New-SPBusinessDataCatalogServiceApplication** cmdlet creates a new Business Data Connectivity service application in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ApplicationPool_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the IIS application pool to use for the new Business Data Connectivity service application.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the **PSCredential** object that contains the user name and password to be used for database SQL Server Authentication.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _DatabaseName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name for the Business Data Connectivity database.  <br/> |
| _DatabasePassword_ <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the password for the user specified in **DatabaseUserName**. Use this parameter only if SQL Server Authentication is used to access the Business Data Connectivity database.  <br/> The type must be a valid password.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the database specified in **DatabaseName**.  <br/> The type must be a valid SQL Server host name; for example, SERVER\Database.  <br/> |
| _DatabaseUsername_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the user name to use for connecting to the database. Use this parameter only if SQL Server Authentication is used to access the Business Data Connectivity database.  <br/> |
| _DeferUpgradeActions_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
| _FailoverDatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the failover database server.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies a display name for the new Business Data Connectivity service application.  <br/> |
| _PartitionMode_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the service application restricts data by subscription ID. This property cannot be changed after the service application is created.  <br/> |
| _Sharing_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the Business Data Connectivity application is published and shared across the farm.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabasePassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseUsername** <br/> |Optional  <br/> |System.String  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Sharing** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Set-SPBusinessDataCatalogServiceApplication](set-spbusinessdatacatalogserviceapplication.md)
  
[New-SPBusinessDataCatalogServiceApplicationProxy](new-spbusinessdatacatalogserviceapplicationproxy.md)

