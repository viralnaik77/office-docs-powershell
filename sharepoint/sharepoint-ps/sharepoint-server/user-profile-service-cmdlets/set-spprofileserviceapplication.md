---
title: "Set-SPProfileServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92948ad5-2100-4b49-a59e-99dfb6a9d1ed

description: "Sets properties of a User Profile Service application."
---

# Set-SPProfileServiceApplication

Sets properties of a User Profile Service application.
  
```
Set-SPProfileServiceApplication <COMMON PARAMETERS>

```

## Example

---------------EXAMPLE---------------------
  
```
$ap = Get-SPServiceApplication -Name PartitionedUserProfileApplication
```

```
#Change the name of the applicationSet-SPProfileServiceApplication -Identity $ap -Name PartitionedUserProfileApplication2
```

This example sets profile information by using the specified identity.
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
The **Set-SPProfileServiceApplication** cmdlet sets properties of a User Profile Service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> |Specifies the User Profile Service application to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a subscription settings service application (for example, SubscriptionSettingsApp1); or an instance of a valid **SPServiceApplication** object.  <br/> |
| _MySiteHostLocation_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the site collection where the My Site will be provisioned.  <br/> The type must be a valid URL, in the form http://server_name; a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a site subscription (for example, SiteSubscription1); or an instance of a valid **SiteSubscription** object.  <br/> |
| _ApplicationPool_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the existing IIS application pool in which to run the Web service for the service application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an application pool (for example, AppPoolName1); or an instance of a valid **IISWebServiceApplicationPool** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _GetNonImportedObjects_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether to inform the users that did not come from the import pipeline and will be marked for deletion. The list of users marked for deletion is displayed to the console window.  <br/> |
| _MySiteManagedPath_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPPrefixPipeBind  <br/> |Specifies the managed path location of personal sites.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the display name for the new User Profile Service application. The name that you use must be a unique name of a User Profile Service application in this farm. The name can be a maximum of 128 characters.  <br/> The type must be a valid name of a User Profile Service application; for example, UserProfileSvcApp1.  <br/> |
| _ProfileDBCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the set of security credentials, such as a user name and a password, that is used to connect to the User Profile database that this cmdlet creates.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _ProfileDBFailoverServer_ <br/> |Optional  <br/> |System.String  <br/> |PARAMVALUE: String  <br/> |
| _ProfileSyncDBCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the set of security credentials, such as a user name and a password, that will be used to connect to the Profile Sync database that is specified in the **ProfileSyncDBName** parameter.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _ProfileSyncDBFailoverServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the failover SQL server for Profile database. It is used to build the connection string for the Profile database.  <br/> |
| _PurgeNonImportedObjects_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether to mark the non-imported users in the profile store for deletion and then inform the users that did not come from the import pipeline which will be marked for deletion. The list of users marked for deletion is displayed on the console window  <br/> |
| _SiteNamingConflictResolution_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the format to use to name personal sites.  <br/> Use one of the following integer values:  <br/> **1** --Personal site collections are to be based on user names without any conflict resolution. For example, http://portal_site/location/username/  <br/> **2** -- Personal site collections are to be based on user names with conflict resolution by using domain names. For example, .../username/ or .../domain_username/  <br/> **3** Personal site collections are to be named by using domain and user name always, to avoid any conflicts. For example, http://portal_site/location/domain_username/  <br/> The default value is **1** (do not resolve conflicts).  <br/> |
| _SocialDBCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |The set of security credentials, including a user name and a password, that is used to connect to the Social database that this cmdlet creates.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _SocialDBFailoverServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the failover SQL server for Social database. It is used to build the connection string for the Social database.  <br/> |
| _UseOnlyPreferredDomainControllers_ <br/> |Optional  <br/> |System.Boolean  <br/> |Restricts profile synchronization communication to a specific domain controller.  <br/> The valid values are $true or $false.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**MySiteHostLocation** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**ApplicationPool** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**GetNonImportedObjects** <br/> |Optional  <br/> |System.Boolean  <br/> ||
|**MySiteManagedPath** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPPrefixPipeBind  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**ProfileDBCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**ProfileDBFailoverServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**ProfileSyncDBCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**ProfileSyncDBFailoverServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**PurgeNonImportedObjects** <br/> |Optional  <br/> |System.Boolean  <br/> ||
|**SiteNamingConflictResolution** <br/> |Optional  <br/> |System.String  <br/> ||
|**SocialDBCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**SocialDBFailoverServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**UseOnlyPreferredDomainControllers** <br/> |Optional  <br/> |System.Boolean  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPProfileServiceApplication](new-spprofileserviceapplication.md)

