---
title: "Set-SPMetadataServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 305625db-541a-454f-b6cd-4a17da74a0b7

description: "Sets the properties of a managed metadata service application."
---

# Set-SPMetadataServiceApplication

Sets the properties of a managed metadata service application.
  
```
Set-SPMetadataServiceApplication -Identity <SPMetadataServiceCmdletPipeBind> <COMMON PARAMETERS>

```

## Example

--------------------EXAMPLE 1---------------------
  
```
Set-SPMetadataServiceApplication -Identity "MetadataServiceApp1" -HubUri "http://sitename" -SyndicationErrorReportEnabled
```

This example adds a content type hub to an existing managed metadata service application. It also enables error reporting when content types are imported. 
  
--------------------EXAMPLE 2---------------------
  
```
Set-SPMetadataServiceApplication -Identity "MetadataServiceApp1" -AdministratorAccount "contoso\username1" -FullAccessAccount "contoso\AppPoolAccount1,contoso\AppPoolAccount2" -RestrictedAccount "contoso\AppPoolAccount3,contoso\AppPoolAccount4,contoso\AppPoolAccount5" -ReadAccessAccount "contoso\AppPoolAccount6"
```

This example sets permissions on an existing managed metadata service application. 
  
> [!NOTE]
> If you use Microsoft PowerShell to set any of the account values, you should set all of them. The **Set-SPMetadataServiceApplication** cmdlet first erases  *all*  accounts, then adds the accounts that you specified. 
  
## Detailed Description

Use the **Set-SPMetadataServiceApplication** cmdlet to set the properties of a managed metadata service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _DisablePartitionQuota_ <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |PARAMVALUE: SwitchParameter  <br/> |
| _GroupsPerPartition_ <br/> |Required  <br/> |System.Int32  <br/> |PARAMVALUE: Int32  <br/> |
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceCmdletPipeBind  <br/> |Specifies the managed metadata service application to update.  <br/> The type must be a valid GUID or the name of a valid managed metadata service application.  <br/> |
| _LabelsPerPartition_ <br/> |Required  <br/> |System.Int32  <br/> |PARAMVALUE: Int32  <br/> |
| _PropertiesPerPartition_ <br/> |Required  <br/> |System.Int32  <br/> |PARAMVALUE: Int32  <br/> |
| _TermSetsPerPartition_ <br/> |Required  <br/> |System.Int32  <br/> |PARAMVALUE: Int32  <br/> |
| _TermsPerPartition_ <br/> |Required  <br/> |System.Int32  <br/> |PARAMVALUE: Int32  <br/> |
| _AdministratorAccount_ <br/> |Optional  <br/> |System.String  <br/> |A comma-separated list of user accounts or service accounts in the format  _\<domain\>_\ _\<account\>_ that may create and run the service application. The accounts must already exist.  <br/> If a value is set by using this parameter, any existing values for the **FullAccessAccount**, **ReadAccessAccount**, and **RestrictedAccount** parameters are removed. Consider setting all four parameters at the same time.  <br/> |
| _ApplicationPool_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies an existing IIS application pool in which to run the Web service for the managed metadata service application.  <br/> The value must be a GUID that is the identity of an **SPServiceApplicationPool** object; the name of an existing application pool; or an instance of a valid **SPServiceApplicationPool** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CacheTimeCheckInterval_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the interval, in seconds, that a front-end Web server should wait before asking the application server for changes. This value is set per timer job, client application, or Web application.  <br/> The mininum value is 1, and there is no maximum value. The default value is **10**.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the **PSCredential** object that contains the user name and password to be used for database SQL authentication.  <br/> If SQL authentication is to be used, either the **DatabaseCredentials** parameter must be specified or both the **DatabaseUserName** and **DatabasePassword** parameters must be set.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _DatabaseName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the database that contains the term store for the managed metadata service application.  <br/> The type must be a valid name of a SQL Server database; for example MeatadataDB1.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the database specified in **DatabaseName**.  <br/> The type must be a valid name of a SQL Server database; for example SqlServerHost1.  <br/> |
| _DoNotUnpublishAllPackages_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |If this flag is set, the packages will not be unpublished. If the **HubUri** parameter is changed, all content type packages will be unpublished by default.  <br/> If the **HubUri** parameter is not changed, this flag has no effect.  <br/> |
| _FailoverDatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the failover database server.  <br/> The type must be a valid SQL Server host name; for example, SQLServerHost1.  <br/> |
| _FullAccessAccount_ <br/> |Optional  <br/> |System.String  <br/> |Specifies a comma-separated set of application pool accounts in the format  _\<domain\>_\ _\<account\>_ that will be given read/write permission to the managed metadata service's term store and content type gallery. The accounts must already exist.  <br/> If a value is set by using this parameter, any existing values for the **AdministratorAccount**, **ReadAccessAccount**, and **RestrictedAccount** parameters are removed. Consider setting all four parameters at the same time.  <br/> |
| _HubUri_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the fully qualified URL of the site collection that contains the content type gallery that the service will provide access to.  <br/> |
| _MaxChannelCache_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of Windows Communication Foundation (WCF) channels that a front-end Web server holds open to the application server. This value is set per timer job, client application, or Web application.  <br/> The minimum value is 0, and there is no maximum value. The default value is **4**.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the new name of the service application. The name can contain a maximum of 128 characters.  <br/> |
| _ReadAccessAccount_ <br/> |Optional  <br/> |System.String  <br/> |Specifies a comma-separated set of application pool accounts in the format  _\<domain\>_\ _\<account\>_ that will be given read-only permission to the managed metadata service's term store and content type gallery. The accounts must already exist.  <br/> If a value is set by using this parameter, any previous values for the **FullAccessAccount**, **RestrictedAccount**, and **AdministratorAccount** parameters are removed. Consider setting all four parameters at the same time.  <br/> |
| _RestrictedAccount_ <br/> |Optional  <br/> |System.String  <br/> |Specifies a comma-separated set of application pool accounts in the format  _\<domain\>_\ _\<account\>_ that will be given permission to read the managed metadata service's term store and content type gallery, and permission to write to open term sets and local term sets and to create new enterprise keywords. The accounts must already exist.  <br/> If a value is set by using this parameter, any previous values for the **FullAccessAccount**, **ReadAccessAccount**, and **AdministratorAccount** parameters are removed. Consider setting all four parameters at the same time.  <br/> |
| _SyndicationErrorReportEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Enables reporting of errors when content types are imported.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceCmdletPipeBind  <br/> ||
|**AdministratorAccount** <br/> |Optional  <br/> |System.String  <br/> ||
|**ApplicationPool** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CacheTimeCheckInterval** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**DoNotUnpublishAllPackages** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**FullAccessAccount** <br/> |Optional  <br/> |System.String  <br/> ||
|**HubUri** <br/> |Optional  <br/> |System.String  <br/> ||
|**MaxChannelCache** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**ReadAccessAccount** <br/> |Optional  <br/> |System.String  <br/> ||
|**RestrictedAccount** <br/> |Optional  <br/> |System.String  <br/> ||
|**SyndicationErrorReportEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPMetadataServiceApplication](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/enterprise-content-management-cmdlets/get-spmetadataserviceapplication.md)
  
[New-SPMetadataServiceApplication](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/enterprise-content-management-cmdlets/new-spmetadataserviceapplication.md)

