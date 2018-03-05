---
title: "Export-SPSiteSubscriptionSettings"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66819487-3225-4341-a9b4-58a369cca05e

description: "Creates a backup file of site subscription data."
---

# Export-SPSiteSubscriptionSettings

Creates a backup file of site subscription data.
  
```
Export-SPSiteSubscriptionSettings [-Identity] <SPSiteSubscriptionPipeBind> -Path <String> [-AdminProperties <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>] [-Force <SwitchParameter>]
```

## Detailed Description

The **Export-SPSiteSubscriptionSettings** cmdlet generates a backup file of all settings in the subscription data store for the given site subscription. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the ID of the site subscription from which to back up data.  <br/> The type must be a valid URL, in the form http://server_name or a GUID in the form 1234-4567-985tg.  <br/> |
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies the location of the output file.  <br/> The type must be a valid path; for example, C:/backupfile.back..  <br/> |
|**AdminProperties** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that only administrator subscription properties are exported. If this parameter is not set, only non-administrator subscription properties are exported.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forces the output backup file (if provided) to overwrite any existing file at the given path.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**AdminProperties** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Get-SPSiteSubscription http://contoso.com | Backup-SPSiteSubscriptionSettings -path "c:/backups"
```

The example backs up the subscription settings store of http://www.contoso.com.
  
## See also

#### 

[Import-SPSiteSubscriptionSettings](import-spsitesubscriptionsettings.md)
  
[Remove-SPSiteSubscriptionSettings](remove-spsitesubscriptionsettings.md)

