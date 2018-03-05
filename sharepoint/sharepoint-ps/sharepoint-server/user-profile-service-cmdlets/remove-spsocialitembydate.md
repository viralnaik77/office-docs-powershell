---
title: "Remove-SPSocialItemByDate"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 640ed571-8711-440e-acf6-3d3a471e7c60

description: "Deletes tags, notes, or ratings."
---

# Remove-SPSocialItemByDate

Deletes tags, notes, or ratings.
  
```
Remove-SPSocialItemByDate -EndDate <DateTime> -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-RemoveComments <$true | $false>] [-RemoveRatings <$true | $false>] [-RemoveTags <$true | $false>] [-SiteSubscription <SPSiteSubscriptionPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Remove-SPSocialItemByDate** cmdlet to delete, tags, notes, ratings created before a particular date. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**EndDate** <br/> |Required  <br/> |System.DateTime  <br/> |Specifies the date before which data is to be deleted.  <br/> |
|**ProfileServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the unique identifier for the proxy.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**RemoveComments** <br/> |Optional  <br/> |System.Boolean  <br/> |When this parameter is specified, comments will be removed.  <br/> Valid values for this parameter are:  <br/> -- **$True** <br/> -- **$False** <br/> |
|**RemoveRatings** <br/> |Optional  <br/> |System.Boolean  <br/> |When this parameter is specified, ratings will be removed.  <br/> Valid values for this parameter are:  <br/> -- **$True** <br/> -- **$False** <br/> |
|**RemoveTags** <br/> |Optional  <br/> |System.Boolean  <br/> |When this parameter is specified, tags will be removed.  <br/> Valid values for this parameter are:  <br/> -- **$True** <br/> -- **$False** <br/> |
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the account under which this service should run. This parameter is mandatory in a hosted-environment and optional in a non-hosted environment.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**EndDate** <br/> |Required  <br/> |System.DateTime  <br/> ||
|**ProfileServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**RemoveComments** <br/> |Optional  <br/> |System.Boolean  <br/> ||
|**RemoveRatings** <br/> |Optional  <br/> |System.Boolean  <br/> ||
|**RemoveTags** <br/> |Optional  <br/> |System.Boolean  <br/> ||
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------EXAMPLE------------
  
```
Remove-SPSocialItemByDate -RemoveTags 1 -ProfileServiceApplicationProxy c6681d53-e6c4-432f-9f31-22d3de81b00c -EndDate 9/15/2009
```

This example removes tags before 9/15/09 from the specified User Profile Service Application Proxy.
  

