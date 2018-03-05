---
title: "Add-SPSiteSubscriptionProfileConfig"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 523ad994-733b-4072-b9e0-d8797ed83dd3

description: "Adds a new site subscription to a User Profile Service application."
---

# Add-SPSiteSubscriptionProfileConfig

Adds a new site subscription to a User Profile Service application.
  
```
Add-SPSiteSubscriptionProfileConfig <COMMON PARAMETERS>

```

## Example

--------------EXAMPLE------------------ 
  
```
#Get UPA Proxy$pr = Get-SPServiceApplicationProxy | ? {$_.DisplayName.Contains(PartitionedUserProfileApplication_Proxy)}
```

```
#Add tenant to UPA Add-SPSiteSubscriptionProfileConfig -Identity $sub -ProfileServiceApplicationProxy $pr -MySiteHostLocation http://contoso/my
```

```
#Create new site subscription$sub = New-SPSiteSubscription
```

This example creates a new User Profile Service application tenant.
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
The **Add-SPSiteSubscriptionProfileConfig** cmdlet adds a new site subscription to a User Profile Service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the proxy of the User Profile Service application to add the site subscription to.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a User Profile Service application proxy (for example, UserProfileSvcProxy1); or an instance of a valid **SPServiceApplicationProxy** object.  <br/> |
| _MySiteHostLocation_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the site collection where the My Site host for the site subscription is provisioned.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid URL, in the form http://server_name; or an instance of a valid **SPSite** object.  <br/> |
| _ProfileServiceApplicationProxy_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the identifier for the User Profile Service Application proxy where the tenant is to be created.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _MySiteManagedPath_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPPrefixPipeBind  <br/> |Specifies the managed path where personal sites will be created.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
| _SiteNamingConflictResolution_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the format to use to name personal sites.  <br/> Use one of the following integer values:  <br/> **1** Personal site collections are to be named based on user names without any conflict resolution. For example, http://portal_site/location/username/  <br/> **2** Personal site collections are to be based on user names with conflict resolution by using domain names. For example, .../username/ or .../domain_username/  <br/> **3** Personal site collections are to be named by using domain and user name always, to avoid any conflicts. For example, http://portal_site/location/domain_username/  <br/> The default value is **1** (do not resolve conflicts).  <br/> |
| _SynchronizationOU_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the organizational unit serving the site subscription.  <br/> The type must be a valid name of an organizational unit; for example, OrgUnit1.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**MySiteHostLocation** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**ProfileServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**MySiteManagedPath** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPPrefixPipeBind  <br/> ||
|**SiteNamingConflictResolution** <br/> |Optional  <br/> |System.String  <br/> ||
|**SynchronizationOU** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Remove-SPSiteSubscriptionProfileConfig](remove-spsitesubscriptionprofileconfig.md)
  
[Set-SPSiteSubscriptionProfileConfig](set-spsitesubscriptionprofileconfig.md)

