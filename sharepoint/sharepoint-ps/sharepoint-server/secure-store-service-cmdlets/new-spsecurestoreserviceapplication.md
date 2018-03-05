---
title: "New-SPSecureStoreServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8e359da-87e6-4e26-92ec-522b18fa965b

description: "Creates a new Secure Store Service application in the farm."
---

# New-SPSecureStoreServiceApplication

Creates a new Secure Store Service application in the farm.
  
```
New-SPSecureStoreServiceApplication -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> -AuditingEnabled <SwitchParameter> [-AssignmentCollection <SPAssignmentCollection>] [-AuditlogMaxSize <Nullable>] [-Confirm [<SwitchParameter>]] [-DatabaseCredentials <PSCredential>] [-DatabaseName <String>] [-DatabasePassword <SecureString>] [-DatabaseServer <String>] [-DatabaseUsername <String>] [-FailoverDatabaseServer <String>] [-Name <String>] [-PartitionMode <SwitchParameter>] [-Sharing <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **New-SPSecureStoreServiceApplication** cmdlet creates a new Secure Store Service application in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPIisWebServiceApplicationPool  <br/> |Specifies the existing IIS application pool to run the Web service in for the new service application.  <br/> |
|**AuditingEnabled** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Turns on auditing for the Secure Store Service.  <br/> |
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the new Secure Store Service application.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**AuditlogMaxSize** <br/> |Optional  <br/> |System.Nullable  <br/> |Specifies the number of days to retain the audit log.  <br/> The type must be a valid integer.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the **PSCredential** object that contains the user name and password to be used for database SQL authentication.  <br/> |
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the Secure Store service database.  <br/> |
|**DatabasePassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the password for the user specified in DatabaseUserName. Use this parameter only if SQL authentication is used to access the metadata service application database.  <br/> |
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the database specified in DatabaseName.  <br/> |
|**DatabaseUsername** <br/> |Optional  <br/> |System.String  <br/> |Specifies the user name to use for connecting to the database for the Secure Store service application. Use this parameter only if SQL authentication is used to access the service application database.  <br/> |
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the failover database server.  <br/> |
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the service application restricts data by subscription ID. This property cannot be changed after the service application is created.  <br/> |
|**Sharing** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the Secure Store service application is published and shared across the farm.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**AuditingEnabled** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**AuditlogMaxSize** <br/> |Optional  <br/> |System.Nullable  <br/> ||
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
   
## Example

------------------EXAMPLE------------------
  
```
New-SPSecureStoreServiceApplication -ApplicationPool "SharePoint Web Services Default" -AuditingEnabled:$false -DatabaseServer "CONTOSO\SharePoint" -DatabaseName "ContosoSSDatabase"-Name "Contoso Secure Store"
```

This example creates a new Secure Store Service application with the name  `Contoso Secure Store` with auditing disabled, and creates a database with the name  `ContosoSSDatabase` on the given database server for use with the service application. 
  
## See also

#### 

[Set-SPSecureStoreServiceApplication](set-spsecurestoreserviceapplication.md)
  
[New-SPSecureStoreServiceApplicationProxy](new-spsecurestoreserviceapplicationproxy.md)

