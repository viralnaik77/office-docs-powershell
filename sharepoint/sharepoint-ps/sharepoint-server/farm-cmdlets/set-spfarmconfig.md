---
title: "Set-SPFarmConfig"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 1/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fc9fd625-0df1-467a-bd31-16b7e29fbca9

description: "Sets a global property or a collection of global properties for the local farm."
---

# Set-SPFarmConfig

Sets a global property or a collection of global properties for the local farm.
  
```
Set-SPFarmConfig [-ASPScriptOptimizationEnabled <$true | $false>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DataFormWebPartAutoRefreshEnabled <$true | $false>] [-DefaultActivateOnSiteMasterValue <$true | $false>] [-Force <SwitchParameter>] [-InstalledProductsRefresh <SwitchParameter>] [-MaxSiteSubscriptionSettingsValueLength <UInt32>] [-MaxTenantStoreValueLength <UInt32>] [-ServiceConnectionPointBindingInformation <String>] [-ServiceConnectionPointDelete <SwitchParameter>] [-SiteMasterMode <Off | On>] [-SiteMasterValidationIntervalInHours <UInt32>] [-UserAccountDirectoryPathIsImmutable <SwitchParameter>] [-WhatIf [<SwitchParameter>]] [-WorkflowBatchSize <Int32>] [-WorkflowEventDeliveryTimeout <Int32>] [-WorkflowPostponeThreshold <Int32>]

```

## Example

---------------------EXAMPLE--------------------------
  
```
$a = Get-SPFarmConfig
```

```
$a.AjaxTimeout = 200
```

```
$a | Set-SPFarmConfig
```

This example uses the  `Get-SPFarmConfig` cmdlet to add the  `Ajax Timeout` setting to the **PSCustomObject** object, sets the value for  `Ajax Timeout`, and then passes **PSCustomObject** to the  `Set-SPFarmConfig` cmdlet to change the  `Ajax Timeout` setting.  `Ajax Timeout`, a farm-wide setting, is a member of the **SPWebService** object and cannot be accessed by using a Windows PowerShell cmdlet. 
  
You can perform the same operations with either of the following commands.
  
```
Set-SPFarmConfig -AjaxTimeout 200
```

## Detailed Description

The **Set-SPFarmConfig** cmdlet updates a collection of global settings for the local farm that are not members of the **SPFarm** object. Use the **Get-SPFarmConfig** cmdlet to read global settings for the local farm and to create a new **PSCustomObject** object from the collection of properties returned from the local farm, and then add this object to the pipeline. Modify the **PSCustomObject** object and pass it to the **Set-SPFarmConfig** cmdlet to change the parameter values. 
  
The properties collected in the **PSCustomObject** object must be farm-wide settings, and must be configurable only once for the entire farm. The parameter name added to the **PSCustomObject** object must match exactly the input parameter name for the **Set-SPFarmConfig** cmdlet. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ASPScriptOptimizationEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies if ASP Script optimization is enabled. The default value is false (off).  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DataFormWebPartAutoRefreshEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether any DataFormWebPart on any page in this farm is allowed to periodically refresh its contents asynchronously (after the page has finished rendering). When set to false, all DataFormWebParts will ignore the automatic refresh interval provided in Web Part properties.  <br/> |
| _DefaultActivateOnSiteMasterValue_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether to activate site master as default.  <br/> |
| _Force_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forces the deletion or updating of the service connection point.  <br/> |
| _InstalledProductsRefresh_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Updates the current machine license state with the list of products that are installed in the farm.  <br/> |
| _MaxSiteSubscriptionSettingsValueLength_ <br/> |Optional  <br/> |System.UInt32  <br/> ||
| _MaxTenantStoreValueLength_ <br/> |Optional  <br/> |System.UInt32  <br/> ||
| _ServiceConnectionPointBindingInformation_ <br/> |Optional  <br/> |System.String  <br/> |Adds or updates the service connection point for the current farm in Active Directory Domain Service (AD DS).  <br/> The type must be an array of strings that are key value pairs that will be added to the service connection point.  <br/> |
| _ServiceConnectionPointDelete_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Delete the service connection point for the current farm in AD DS.  <br/> |
| _SiteMasterMode_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPSiteMasterMode  <br/> |Specifies if site master mode is turned on or off. The default value is off.  <br/> |
| _SiteMasterValidationIntervalInHours_ <br/> |Optional  <br/> |System.UInt32  <br/> ||
| _UserAccountDirectoryPathIsImmutable_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WorkflowBatchSize_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the paging size for events delivered to a single workflow instance. For each request, the events are streamed out 100 at a time.  <br/> Batch size is the number of events processed for a single workflow instance, which can have many events queued at the same time. Throttle will override batch size; if the workflow instance cannot be started or restarted because there are too many instances running across all front-end Web servers, none of the events will be fetched, regardless of the batch size.  <br/> |
| _WorkflowEventDeliveryTimeout_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the time as an integer in which a workflow job must run without the job timing out. If the workflow job does time out, it gets put back in the queue to be run again.  <br/> For example, if the value is set to 5, the workflow job must run within 5 minutes are the workflow job will time out. Any workflow job that does time out is placed back in the queue to run again. The default value is **5**.  <br/> |
| _WorkflowPostponeThreshold_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of workflows that can be running in IIS against a content database at a time before new workflow instances get postponed into a queue.  <br/> |
   
## See also

#### 

[Get-SPFarmConfig](get-spfarmconfig.md)

