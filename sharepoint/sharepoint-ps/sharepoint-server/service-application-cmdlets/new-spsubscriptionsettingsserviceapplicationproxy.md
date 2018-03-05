---
title: "New-SPSubscriptionSettingsServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7ce4a42-a36f-4ef6-b8c1-bdd77e23d999

description: "Creates an application proxy to a subscription settings service application."
---

# New-SPSubscriptionSettingsServiceApplicationProxy

Creates an application proxy to a subscription settings service application.
  
```
New-SPSubscriptionSettingsServiceApplicationProxy -Uri <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **New-SPSubscriptionSettingsServiceApplicationProxy** cmdlet to create an application proxy to a subscription settings service application. This is required for the local farm to consume a subscription settings service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> |Specifies the subscription settings service application associated with the new proxy.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a subscription settings service application (for example, SubscriptionSettingsApp1); or an instance of a valid **SPServiceApplication** object.  <br/> |
|**Uri** <br/> |Required  <br/> |System.String  <br/> |Specifies the address of the subscription settings service application to associate the new application proxy with.  <br/> The type must be a valid URI, in the form file:\\server_name\sitedocs.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**Uri** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------------EXAMPLE---------------------------
  
```
$AppPool = New-SPIisWebServiceApplicationPool -Name SettingsServiceAppPool -Account (Get-SPManagedAccount DOMAIN\jdoe)
```

```
$App = New-SPSubscriptionSettingsServiceApplication -ApplicationPool $appPool -Name SettingsServiceApp -DatabaseName SettingsServiceDB
```

```
$proxy = New-SPSubscriptionSettingsServiceApplicationProxy -ServiceApplication $App
```

```
Get-SPServiceInstance | where{$_.TypeName -eq "Microsoft SharePoint Foundation Subscription Settings Service"} | Start-SPServiceInstance
```

This example creates an application pool, a new settings service application, a settings service application proxy, and then starts the service instance on the local machine. This example assumes that a managed account for  `DOMAIN\jdoe` already exists. 
  
## See also

#### 

[New-SPSubscriptionSettingsServiceApplication](new-spsubscriptionsettingsserviceapplication.md)
  
[Set-SPSubscriptionSettingsServiceApplication](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/site-management-cmdlets/set-spsubscriptionsettingsserviceapplication.md)

