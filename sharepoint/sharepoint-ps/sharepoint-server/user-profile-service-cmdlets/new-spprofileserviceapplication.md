---
title: "New-SPProfileServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acf51379-1811-4ffe-b5a0-a660d7a58f10

description: "Adds a User Profile Service application to a farm."
---

# New-SPProfileServiceApplication

Adds a User Profile Service application to a farm.
  
```
New-SPProfileServiceApplication <COMMON PARAMETERS>

```

## Example

----------------------EXAMPLE------------------------- 
  
```
$appPool = New-SPIisWebServiceApplicationPool -Name HostedAppPool -Account (Get-SPManagedAccount "contoso\AppPoolAccount")New-SPProfileServiceApplication -Name PartitionedUserProfileApplication -PartitionMode -ApplicationPool $appPool
```

This example creates a new User Profile Service application.
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
The **New-SPProfileServiceApplication** cmdlet adds and creates a new profile service application, or creates an instance of a profile service. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ApplicationPool_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the existing IIS application pool in which to run the Web service for the service application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an application pool (for example, AppPoolName1); or an instance of a valid **IISWebServiceApplicationPool** object.  <br/> |
| _MySiteHostLocation_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the site collection where the My Site will be created.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid URL, in the form http://server_name; or an instance of a valid **SPSite** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DeferUpgradeActions_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |PARAMVALUE: SwitchParameter  <br/> |
| _MySiteManagedPath_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPPrefixPipeBind  <br/> |Specifies the managed path where personal sites will be created.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the display name for the new User Profile Service application. The name must be a unique name of a User Profile Service application in this farm. The name can be a maximum of 64 characters.  <br/> The type must be a valid name of a service application; for example, UserProfileSvcApp1.  <br/> |
| _PartitionMode_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the service application restrict data by site group. After the **PartitionMode** parameter is set and the service application is created, it cannot be changed.  <br/> |
| _ProfileDBCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the set of security credentials, such as a user name and a password, that is used to connect to the User Profile database that this cmdlet creates.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _ProfileDBFailoverServer_ <br/> |Optional  <br/> |System.String  <br/> |Associates a content database with a specific failover server that is used in conjunction with SQL Server database mirroring. The server name is the required value.  <br/> |
| _ProfileDBName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the database where the User Profile database is created.  <br/> |
| _ProfileDBServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the database where the User Profile database will be created.  <br/> The type must be a valid name of a SQL Server database; for example, ProfileAppDB1.  <br/> |
| _ProfileSyncDBCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the set of security credentials, such as a user name and a password, that will be used to connect to the Profile Sync database that is specified in the **ProfileSyncDBName** parameter.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _ProfileSyncDBFailoverServer_ <br/> |Optional  <br/> |System.String  <br/> |Associates a Profile Sync database with a specific failover server that is used in conjunction with SQL Server database mirroring. The server name is the required value.  <br/> |
| _ProfileSyncDBName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the database where the Profile Sync database will be created.  <br/> The type must be a valid name of a SQL Server database; for example, ProfileSyncAppDB1.  <br/> |
| _ProfileSyncDBServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the database server that will host the Profile Sync database that is specified in the **ProfileSyncDBName** parameter.  <br/> The type must be a valid name of a SQL Server host; for example, SQLServerProfileSyncHost1.  <br/> |
| _SiteNamingConflictResolution_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the format to use to name personal sites.  <br/> Use one of the following integer values:  <br/> **1** Personal site collections are to be based on user names without any conflict resolution. For example, http://portal_site/location/username/  <br/> **2** Personal site collections are to be based on user names with conflict resolution by using domain names. For example, .../username/ or .../domain_username/  <br/> **3** Personal site collections are to be named by using domain and user name always, to avoid any conflicts. For example, http://portal_site/location/domain_username/  <br/> The default value is **1** (do not resolve conflicts).  <br/> |
| _SocialDBCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |The set of security credentials, including a user name and a password, that is used to connect to the Social database that this cmdlet creates.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _SocialDBFailoverServer_ <br/> |Optional  <br/> |System.String  <br/> |Associates a Social database with a specific failover server that is used in conjunction with SQL Server database mirroring. The server name is the required value.  <br/> |
| _SocialDBName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the database where the Social database will be created.  <br/> The type must be a valid name of a SQL Server host; for example, SQLServerSocialHost1.  <br/> |
| _SocialDBServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the database server that will host the Social database that is specified in **SocialDBName**.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**MySiteHostLocation** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**MySiteManagedPath** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPPrefixPipeBind  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ProfileDBCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**ProfileDBFailoverServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**ProfileDBName** <br/> |Optional  <br/> |System.String  <br/> ||
|**ProfileDBServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**ProfileSyncDBCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**ProfileSyncDBFailoverServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**ProfileSyncDBName** <br/> |Optional  <br/> |System.String  <br/> ||
|**ProfileSyncDBServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**SiteNamingConflictResolution** <br/> |Optional  <br/> |System.String  <br/> ||
|**SocialDBCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**SocialDBFailoverServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**SocialDBName** <br/> |Optional  <br/> |System.String  <br/> ||
|**SocialDBServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Set-SPProfileServiceApplication](set-spprofileserviceapplication.md)

