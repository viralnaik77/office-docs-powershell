---
title: "Use Windows PowerShell cmdlets to manage performance in SharePoint Server 2016"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 2/25/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: 3052280d-7cbd-4d43-b31f-ab89dc438131
description: "Summary: Learn about the Windows PowerShell cmdlets that you can use to manage performance for SharePoint Server 2016."
---

# Use Windows PowerShell cmdlets to manage performance in SharePoint Server 2016

 **Summary:** Learn about the Windows PowerShell cmdlets that you can use to manage performance for SharePoint Server 2016. 
  
The following table shows the Microsoft PowerShell cmdlets that you can use to manage performance for a SharePoint Server 2016 farm.
  
[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md) includes a complete list of all cmdlets in SharePoint Server 2016. 
  
|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Add-SPDiagnosticsPerformanceCounter](add-spdiagnosticsperformancecounter.md)** <br/> |Adds an instance of a performance counter.  <br/> |
|**[Get-SPDiagnosticsPerformanceCounter](get-spdiagnosticsperformancecounter.md)** <br/> |Returns a collection of performance counters.  <br/> |
|**[Remove-SPDiagnosticsPerformanceCounter](remove-spdiagnosticsperformancecounter.md)** <br/> |Removes an instance of a performance counter.  <br/> |
|**[Disable-SPWebApplicationHttpThrottling](disable-spwebapplicationhttpthrottling.md)** <br/> |Turns off network throttling for a web application.  <br/> |
|**[Enable-SPWebApplicationHttpThrottling](enable-spwebapplicationhttpthrottling.md)** <br/> |Turns on network throttling for a web application.  <br/> |
|**[Get-SPBusinessDataCatalogThrottleConfig](get-spbusinessdatacatalogthrottleconfig.md)** <br/> |Returns the throttling configuration for a Business Data Connectivity Service application.  <br/> |
|**[Set-SPBusinessDataCatalogThrottleConfig](set-spbusinessdatacatalogthrottleconfig.md)** <br/> |Sets the throttling configuration for a Business Data Connectivity Service application.  <br/> |
|**[Get-SPWebApplicationHttpThrottlingMonitor](get-spwebapplicationhttpthrottlingmonitor.md)** <br/> |Reads all counters for network throttling on a web application.  <br/> |
|**[Set-SPWebApplicationHttpThrottlingMonitor](set-spwebapplicationhttpthrottlingmonitor.md)** <br/> |Sets the Health Score bucket values for an existing network throttling performance counter for a specified web application.  <br/> |
|**[Start-SPDiagnosticsSession](start-spdiagnosticssession.md)** <br/> |Reports diagnostic information to the usage database.  <br/> |
|**[Stop-SPDiagnosticsSession](stop-spdiagnosticssession.md)** <br/> |Stops the diagnostics session.  <br/> |
|**[Add-SPRoutingMachineInfo](add-sproutingmachineinfo.md)** <br/> |Adds a new routing target to the farm.  <br/> |
|**[Add-SPRoutingMachinePool](add-sproutingmachinepool.md)** <br/> |Adds a new machine pool.  <br/> |
|**[Add-SPRoutingRule](add-sproutingrule.md)** <br/> |Adds a routing rule.  <br/> |
|**[Add-SPThrottlingRule](add-spthrottlingrule.md)** <br/> |Adds a new throttling rule.  <br/> |
|**[Get-SPRoutingMachineInfo](get-sproutingmachineinfo.md)** <br/> |Returns all the routing targets.  <br/> |
|**[Get-SPRoutingMachinePool](get-sproutingmachinepool.md)** <br/> |Returns all available routing pools.  <br/> |
|**[Get-SPRoutingRule](get-sproutingrule.md)** <br/> |Returns all routing rules.  <br/> |
|**[Get-SPThrottlingRule](get-spthrottlingrule.md)** <br/> |Returns all throttling rules.  <br/> |
|**[Remove-SPRoutingMachineInfo](remove-sproutingmachineinfo.md)** <br/> |Removes an external routing target.  <br/> |
|**[Remove-SPRoutingMachinePool](remove-sproutingmachinepool.md)** <br/> |Removes a routing pool from Request Manager.  <br/> |
|**[Remove-SPRoutingRule](remove-sproutingrule.md)** <br/> |Removes a routing rule.  <br/> |
|**[Remove-SPThrottlingRule](remove-spthrottlingrule.md)** <br/> |Removes a throttling rule.  <br/> |
|**[Set-SPRoutingMachineInfo](set-sproutingmachineinfo.md)** <br/> |Sets routing target properties.  <br/> |
|**[Set-SPRoutingMachinePool](set-sproutingmachinepool.md)** <br/> |Sets properties of a machine pool.  <br/> |
|**[Set-SPRoutingRule](set-sproutingrule.md)** <br/> |Changes properties of an existing routing rule.  <br/> |
|**[Set-SPThrottlingRule](set-spthrottlingrule.md)** <br/> |Changes properties of an existing throttling rule.  <br/> |
|**[Get-SPRequestManagementSettings](get-sprequestmanagementsettings.md)** <br/> |Returns a Request Manager object.  <br/> |
|**[New-SPRequestManagementRuleCriteria](new-sprequestmanagementrulecriteria.md)** <br/> |Creates criteria for the rule to match.  <br/> |
|**[Set-SPRequestManagementSettings](set-sprequestmanagementsettings.md)** <br/> |Sets Request Manager properties.  <br/> |
|**[Get-SPDistributedCacheClientSetting](get-spdistributedcacheclientsetting.md)** <br/> |Returns distributed cache settings from usage.  <br/> |
|**[Clear-SPDistributedCacheItem](clear-spdistributedcacheitem.md)** <br/> |Clears cached items from the distributed cache server.  <br/> |
|**[Set-SPDistributedCacheClientSetting](set-spdistributedcacheclientsetting.md)** <br/> |Sets distributed cache settings.  <br/> |
|**[Stop-SPDistributedCacheServiceInstanceGracefullyOnLocalServer](http://technet.microsoft.com/library/e0859f65-e9e3-43c3-aa0d-bbe5953defc7.aspx)** <br/> |Obsolete. For replacement, see [Stop-SPDistributedCacheServiceInstance](stop-spdistributedcacheserviceinstance.md) <br/> |
|**[Stop-SPDistributedCacheServiceInstance](stop-spdistributedcacheserviceinstance.md)** <br/> |Stops an instance of the distributed cache service on a local server.  <br/> |
|**[Remove-SPDistributedCacheServiceInstanceOnLocalServer](http://technet.microsoft.com/library/d4d1a1f8-eab5-4ae2-8aa0-f25ee807a505.aspx)** <br/> |Obsolete. For replacement, see [Remove-SPDistributedCacheServiceInstance](remove-spdistributedcacheserviceinstance.md) <br/> |
|**[Remove-SPDistributedCacheServiceInstance](remove-spdistributedcacheserviceinstance.md)** <br/> |Removes an instance of the distributed cache service from a local server.  <br/> |
|**[Add-SPDistributedCacheServiceInstanceOnLocalServer](http://technet.microsoft.com/library/28c64abc-fdf8-4353-ac9f-05e9ad8e509d.aspx)** <br/> |Obsolete. For replacement, see [Add-SPDistributedCacheServiceInstance](add-spdistributedcacheserviceinstance.md) <br/> |
|**[Add-SPDistributedCacheServiceInstance](add-spdistributedcacheserviceinstance.md)** <br/> |Adds an instance of the distributed cache service to a local server.  <br/> |
|[Update-SPDistributedCacheSize](update-spdistributedcachesize.md) <br/> |Reconfigures the allocation of memory that is dedicated to the Distributed Cache service.  <br/> |
   
## See also

#### 

[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md)

