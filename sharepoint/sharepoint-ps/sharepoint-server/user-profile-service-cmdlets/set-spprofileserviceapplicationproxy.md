---
title: "Set-SPProfileServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/7/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1453024d-9078-47a4-b1a8-d4b600226442

description: "Sets properties of a proxy for a User Profile Service application."
---

# Set-SPProfileServiceApplicationProxy

Sets properties of a proxy for a User Profile Service application.
  
```
Set-SPProfileServiceApplicationProxy [-Identity] <SPServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DefaultProxyGroup <SwitchParameter>] [-MySiteHostLocation <SPSitePipeBind>] [-MySiteManagedPath <SPPrefixPipeBind>] [-Name <String>] [-SiteNamingConflictResolution <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPProfileServiceApplicationProxy** cmdlet sets properties of a proxy for a User Profile Service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the User Profile Service application proxy to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a service application proxy (for example, UserProfileSvcProxy1); or an instance of a valid **SPServiceApplicationProxy** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the User Profile Service application proxy is added to the default proxy group for the local farm.  <br/> |
|**MySiteHostLocation** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the site collection where the My Site will be created.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid URL, in the form http://server_name; or an instance of a valid **SPSite** object.  <br/> |
|**MySiteManagedPath** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPPrefixPipeBind  <br/> |Specifies the managed path location of personal sites.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the display name for the User Profile Service application. The name that you use must be a unique name of a User Profile Service application in this farm. The name can be a maximum of 128 characters.  <br/> The type must be a name of a valid service application proxy; for example, UserProfileSvcProxy1.  <br/> |
|**SiteNamingConflictResolution** <br/> |Optional  <br/> |System.String  <br/> |Specifies the format to use to name personal sites.  <br/> Use one of the following integer values:  <br/> **1** Personal site collections are to be based on user names without any conflict resolution. For example, http://portal_site/location/username/  <br/> **2** Personal site collections are to be based on user names with conflict resolution by using domain names. For example, .../username/ or .../domain_username/  <br/> **3** Personal site collections are to be named by using domain and user name always, to avoid any conflicts. For example, http://portal_site/location/domain_username/  <br/> The default value is **1** (do not resolve conflicts).  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**MySiteHostLocation** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**MySiteManagedPath** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPPrefixPipeBind  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**SiteNamingConflictResolution** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

----------------EXAMPLE--------------------- 
  
```
#Get UPA Proxy
$pr = Get-SPServiceApplicationProxy | ? {$_.DisplayName.Contains("PartitionedUserProfileApplication_Proxy")}
```

```
#Change the name of the proxy
Set-SPProfileServiceApplicationProxy -Identity $pr -Name PartitionedUserProfileApplication_Proxy2
```

This example sets a proxy for the User Profile Service application.
  
## See also

#### 

[New-SPProfileServiceApplicationProxy](new-spprofileserviceapplicationproxy.md)

