---
title: "Set-SPAppHostingQuotaConfiguration"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 681231c0-baa7-4313-adfc-8470413d47bb

description: "Sets hosting quotas for an app."
---

# Set-SPAppHostingQuotaConfiguration

Sets hosting quotas for an app.
  
```
Set-SPAppHostingQuotaConfiguration -AppHostingLicenseQuota <Double> -AppInstanceCountQuota <Double> -SiteSubscription <SPSiteSubscriptionPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Set-SPAppHostingQuotaConfiguration** cmdlet to set hosting quotas for a specified app by using the **Identity** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppHostingLicenseQuota** <br/> |Required  <br/> |System.Double  <br/> |Specifies the app licensing quota.  <br/> |
|**AppInstanceCountQuota** <br/> |Required  <br/> |System.Double  <br/> |Specifies the number instances of an app.  <br/> |
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the site for which to set hosting quotas.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppHostingLicenseQuota** <br/> |Required  <br/> |System.Double  <br/> ||
|**AppInstanceCountQuota** <br/> |Required  <br/> |System.Double  <br/> ||
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

----------------EXAMPLE 1----------
  
```
Set-SPAppHostingQuotaConfiguration -Identity 586d4a32-98c3-42ce-80be-3c76c10c250c -AppInstanceCountQuota 50 -AppHostingLicenseQuota 25
```

This example sets hosting Quotas for the SiteSubscriptionId "586d4a32-98c3-42ce-80be-3c76c10c250c" with hosted appinstance limit as 50 and hosted apps licenses assigned as 25.
  
----------------EXAMPLE 2----------
  
```
Get-SPSiteSubscription | Set-SPAppHostingQuotaConfiguration -Identity $_ -AppInstanceCountQuota 50 -AppHostingLicenseQuota 25
```

This example sets hosting Quotas for all SiteSubscriptions in the farm with hosted apps limit as 50 and hosted apps licenses assigned as 25.
  
## See also

#### 

[Get-SPAppHostingQuotaConfiguration](get-spapphostingquotaconfiguration.md)

