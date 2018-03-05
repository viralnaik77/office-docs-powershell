---
title: "Set-SPAccessServicesApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/20/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e7b805f1-1325-4625-8087-e8b0042ed292

description: "Sets global properties of an existing Access Services application in SharePoint Server 2016."
---

# Set-SPAccessServicesApplication

Sets global properties of an existing Access Services application in SharePoint Server 2016.
  
```
Set-SPAccessServicesApplication -Identity <SPServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-CacheTimeout <Int32>] [-Confirm [<SwitchParameter>]] [-PrivateBytesMax <Int32>] [-RecoveryPointObjective <Int32>] [-RequestDurationMax <Int32>] [-SessionsPerAnonymousUserMax <Int32>] [-SessionsPerUserMax <Int32>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------EXAMPLE 1------------------
  
```
Set-SPAccessServiceApplication -Identity "MyAccessService" -RequestDurationMax 100
```

This example sets the Access Services application named  `MyAccessService` to let requests take up to  `100` seconds before they time out. 
  
------------EXAMPLE 2------------------
  
```
Get-SPAccessServiceApplication | Set-SPAccessServiceApplication -SessionsPerUserMax 5
```

This example sets every Access Services application in the farm to allow up to five sessions per user on each back-end application server computer on which Access Services runs.
  
First, every Access Services application is returned, and then a new value is set by using the **Set-SPAccessServiceApplication** cmdlet. 
  
## Detailed Description

The **Set-SPAccessServiceApplication** cmdlet sets the global runtime properties of an existing Access Services application in SharePoint Server 2016. If you use this cmdlet to update properties, updates affect all servers in the farm on which this Access Services application runs. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> | Specifies the Access Services application to update.  <br/>  The value must be in one of the following forms:  <br/>  A valid name of an Access Services application; for example, AccessSrvApp1  <br/>  A valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh  <br/>  An instance of a valid **SPAccessServiceApplication** object  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CacheTimeout_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of seconds that a data cache will remain active on Access Services with no user activity. Valid values include: -1, cache never times out; 1 to 2073600, cache remains active from 1 second to 24 days.  <br/> The type must be the integers -1, or an integer in the range of 1 to 2073600 (24 days). The default value is **300**.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _PrivateBytesMax_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum private bytes in megabytes that can be used by Access Services. When set to -1, it defaults to 75 percent of physical memory on the server. Valid values: -1, no limit, from 1 to any positive integer.The default value is - **1**.  <br/> |
| _RecoveryPointObjective_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum amount of time in minutes by which the replica can fall behind the primary before the primary is read-only when geo-replication is used.  <br/> |
| _RequestDurationMax_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of seconds that a request to perform an operation can use before the request times out. Valid values include: -1, no limit, 1 to 2073600, cache remains active 1 second to 24 days. The default value is **30**.  <br/> The type must be the integer -1, or an integer in the range of 1 to 2073600 (24 days)  <br/> |
| _SessionsPerAnonymousUserMax_ <br/> |Optional  <br/> |System.Int32  <br/> |The maximum number of sessions allowed per user. If this maximum is exceeded, the oldest session will be deleted when a new session is started. Valid values include: -1, no limit, and 1 to any positive integer. The default value is **10**.  <br/> The integer -1, or an integer in the range of 1 to MaxInt  <br/> |
| _SessionsPerUserMax_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of sessions allowed per user. If this maximum is exceeded, the oldest session is deleted when a new session is started. Valid values include: -1, no limit, and 1 to any positive integer. The default value is **10**.  <br/> The integer -1, or an integer in the range of 1 to MaxInt.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CacheTimeout** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**PrivateBytesMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**RequestDurationMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**SessionsPerAnonymousUserMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**SessionsPerUserMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPAccessServicesApplication](get-spaccessservicesapplication.md)
  
[New-SPAccessServicesApplication](new-spaccessservicesapplication.md)

