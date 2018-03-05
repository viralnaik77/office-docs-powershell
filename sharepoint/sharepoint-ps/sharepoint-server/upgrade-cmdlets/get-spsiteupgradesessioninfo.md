---
title: "Get-SPSiteUpgradeSessionInfo"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e16dd385-1e08-4325-8318-e19e4b752868

description: "Manage or report site upgrade."
---

# Get-SPSiteUpgradeSessionInfo

Manage or report site upgrade.
  
```
Get-SPSiteUpgradeSessionInfo -ContentDatabase <SPContentDatabasePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-HideWaiting <SwitchParameter>] [-ShowCompleted <SwitchParameter>] [-ShowFailed <SwitchParameter>] [-ShowInProgress <SwitchParameter>] [-SiteSubscription <SPSiteSubscriptionPipeBind>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **Get-SPSiteUpgradeSessionInfo** cmdlet to manage or report site upgrade of the farm. 
  
This cmdlet has two modes, get upgrade information for a specific **SPSite** object or for a given content database. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ContentDatabase** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the GUID of the content database from which to list site collections.The type must be a valid database name, in the form SPContentDB01, or a valid GUID (for example, 12345678-90ab-cdef-1234-567890bcdefgh).  <br/> |
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the site of which you want to report.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**HideWaiting** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to hide site collections that upgrade has not started.  <br/> |
|**ShowCompleted** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to show site collections that has completed upgrade.  <br/> |
|**ShowFailed** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to show site collections that have failed upgrade.  <br/> |
|**ShowInProgress** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays site collections that are in the process of being upgraded.  <br/> |
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies to limit the result to site collections within the site subscription.  <br/> |
   
## Example

-----------EXAMPLE 1---------- 
  
```
$db = Get-SPContentDatabase -Identity wss_content
```

```
Get-SPSiteUpgradeSessionInfo -ContentDatabase $db
```

This example returns siteupgradeinfo for every SPContentDatabase returned from **Get-SPContentDatabase** cmdlet. 
  
-----------EXAMPLE 2---------- 
  
```
$site=Get-SPSite -Identity http://localhost
```

```
Get-SPSiteUpgradeSessionInfo -Site $site
```

This example returns siteupgradeinfo for every SPSite object returned from **Get-SPSite** cmdlet. 
  
## See also

#### 

[Remove-SPSiteUpgradeSessionInfo](remove-spsiteupgradesessioninfo.md)

