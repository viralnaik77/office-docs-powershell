---
title: "New-SPMetadataServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 03f561ed-ab75-4feb-bd55-b57f8638619f

description: "Creates a new managed metadata service application."
---

# New-SPMetadataServiceApplication

Creates a new managed metadata service application.
  
```
New-SPMetadataServiceApplication -Name <String> <COMMON PARAMETERS>

```

## Example

-------------------EXAMPLE 1-------------
  
```
New-SPMetadataServiceApplication -Name "MetadataServiceApp1" -ApplicationPool "AppPool1" -DatabaseName "MetadataDB1"
```

This example creates a new managed metadata service application.
  
-------------------EXAMPLE 2-------------
  
```
New-SPMetadataServiceApplication -Name "MetadataServiceApp2" -ApplicationPool "AppPool1" -DatabaseName "MetadataDB2" -HubUri "http://sitename" -SyndicationErrorReportEnabled
```

This example creates a new managed metadata service application and specifies a content type hub to be used for syndication. It also enables error reporting during syndication.
  
-------------------EXAMPLE 3-------------
  
```
New-SPMetadataServiceApplication -Name "MetadataServiceApp3" -ApplicationPool "AppPool1" -DatabaseName "MetadataDB3" -PartitionMode
```

This example creates a new managed metadata service application that is partitioned, for use by sites in a subscription.
  
## Detailed Description

Use the **New-SPMetadataServiceApplication** cmdlet to create a new managed metadata service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ApplicationPool_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies an existing IIS application pool in which to run the new managed metadata service application.  <br/> The value must be a GUID that is the identity of an **SPServiceApplicationPool** object; the name of an existing application pool, or an instance of an **SPServiceApplicationPool** object.  <br/> |
| _DisablePartitionQuota_ <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |PARAMVALUE: SwitchParameter  <br/> |
| _GroupsPerPartition_ <br/> |Required  <br/> |System.Int32  <br/> |PARAMVALUE: Int32  <br/> |
| _LabelsPerPartition_ <br/> |Required  <br/> |System.Int32  <br/> |PARAMVALUE: Int32  <br/> |
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the service application to create. The name can contain a maximum of 128 characters.  <br/> |
| _PropertiesPerPartition_ <br/> |Required  <br/> |System.Int32  <br/> |PARAMVALUE: Int32  <br/> |
| _TermSetsPerPartition_ <br/> |Required  <br/> |System.Int32  <br/> |PARAMVALUE: Int32  <br/> |
| _TermsPerPartition_ <br/> |Required  <br/> |System.Int32  <br/> |PARAMVALUE: Int32  <br/> |
| _AdministratorAccount_ <br/> |Optional  <br/> |System.String  <br/> |A comma-separated list of user accounts or service accounts in the format  _\<domain\>_\ _\<account\>_ that may create and run the service application. The accounts must already exist.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CacheTimeCheckInterval_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies an interval, in seconds, that a front-end Web Server should wait before asking the application server for changes. This value is set per timer job, client application, or Web application.  <br/> The mininum value is 1, and there is no maximum value. The default value is **10**.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the **PSCredential** object that contains the user name and password to be used for database SQL authentication.  <br/> If SQL authentication is to be used, either **DatabaseCredentials** must be specified or both the **DatabaseUserName** and **DatabasePassword** parameters must be set.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _DatabaseName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the database to create for the new managed metadata service application.  <br/> The type must be a valid name of a SQL Server database; for example MeatadataDB1.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the database specified in **DatabaseName**.  <br/> The type must be a valid name of a SQL Server database; for example SqlServerHost1.  <br/> |
| _DeferUpgradeActions_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |PARAMVALUE: SwitchParameter  <br/> |
| _FailoverDatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the failover database server.  <br/> The type must be a valid SQL Server host name; for example, SQLServerHost1.  <br/> |
| _FullAccessAccount_ <br/> |Optional  <br/> |System.String  <br/> |Specifies a comma-separated set of application pool accounts in the format  _\<domain\>_\ _\<account\>_ that will be given read/write permission to the managed metadata service's term store and content type gallery. The accounts must already exist.  <br/> |
| _HubUri_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the fully qualified URL of the site collection that contains the content type gallery that the service will provide access to.  <br/> |
| _MaxChannelCache_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of Windows Communication Foundation (WCF) channels that a front-end Web server should hold open to the application server. This value is set per timer job, client application, or Web application.  <br/> The minimum value is 0, and there is no maximum value. The default value is **4**.  <br/> |
| _PartitionMode_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the service application restrict data by subscription.  <br/> **Note** This property cannot be changed after the service application has been created.  <br/> |
| _ReadAccessAccount_ <br/> |Optional  <br/> |System.String  <br/> |Specifies a comma-separated set of application pool accounts in the format  _\<domain\>_\ _\<account\>_ that will be given read-only permission to the managed metadata service's term store and content type gallery. The accounts must already exist.  <br/> |
| _RestrictedAccount_ <br/> |Optional  <br/> |System.String  <br/> |Specifies a comma-separated set of application pool accounts in the format  _\<domain\>_\ _\<account\>_ that will be given permission to read the managed metadata service's term store and content type gallery, and permission to write to open term sets and local term sets and to create new enterprise keywords. The accounts must already exist.  <br/> |
| _SyndicationErrorReportEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Enables reporting of errors when content types are imported.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**AdministratorAccount** <br/> |Optional  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CacheTimeCheckInterval** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**FullAccessAccount** <br/> |Optional  <br/> |System.String  <br/> ||
|**HubUri** <br/> |Optional  <br/> |System.String  <br/> ||
|**MaxChannelCache** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ReadAccessAccount** <br/> |Optional  <br/> |System.String  <br/> ||
|**RestrictedAccount** <br/> |Optional  <br/> |System.String  <br/> ||
|**SyndicationErrorReportEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPMetadataServiceApplication](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/enterprise-content-management-cmdlets/get-spmetadataserviceapplication.md)
  
[Set-SPMetadataServiceApplication](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/enterprise-content-management-cmdlets/set-spmetadataserviceapplication.md)

