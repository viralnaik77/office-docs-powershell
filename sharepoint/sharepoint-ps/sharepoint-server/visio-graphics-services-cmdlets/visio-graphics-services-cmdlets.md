---
title: "Visio Graphics Services cmdlets in SharePoint Server 2016"
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
ms.assetid: 1e01d97d-ce72-4410-b751-9187a0e8b6bf
description: "Summary: Lists Windows PowerShell cmdlets that help you administer the Visio Graphics Service in SharePoint Server 2016."
---

# Visio Graphics Services cmdlets in SharePoint Server 2016

 **Summary:** Lists Windows PowerShell cmdlets that help you administer the Visio Graphics Service in SharePoint Server 2016. 
  
Visio Graphics Service is a service in SharePoint Server 2016 that users can use to view published Visio diagrams. The service also refreshes published Visio diagrams that are connected to supported data sources.
  
All Visio Graphics Service settings will support backup and recovery, regardless of whether there is a UI setting. This means all global settings will support backup and restore operations.
  
The Visio Graphics Service has PowerShell functionality that you can use to provision a new instance, manage and configure available data sources, manage and configure a list of safe data providers, and configure all the global settings of the service.
  
[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md) includes a complete list of all cmdlets in SharePoint Server 2016. 
  
|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Get-SPVisioExternalData](get-spvisioexternaldata.md)** <br/> |Returns the settings for external data connections for a Visio Services application.  <br/> |
|**[Get-SPVisioPerformance](get-spvisioperformance.md)** <br/> |Returns the Visio Services settings for the performance of a Visio Services application.  <br/> |
|**[Get-SPVisioSafeDataProvider](get-spvisiosafedataprovider.md)** <br/> |Returns the settings of a safe data provider for a Visio Services application.  <br/> |
|**[Get-SPVisioServiceApplication](get-spvisioserviceapplication.md)** <br/> |Returns properties of a Visio Services application or a collection of Visio Services applications.  <br/> |
|**[Get-SPVisioServiceApplicationProxy](get-spvisioserviceapplicationproxy.md)** <br/> |Returns properties of a Visio Services application proxy or a collection of Visio Services application proxies  <br/> |
|**[New-SPVisioSafeDataProvider](new-spvisiosafedataprovider.md)** <br/> |Adds a new data provider to a Visio Services application.  <br/> |
|**[New-SPVisioServiceApplication](new-spvisioserviceapplication.md)** <br/> |Adds a new Visio Services application to a farm.  <br/> |
|**[New-SPVisioServiceApplicationProxy](new-spvisioserviceapplicationproxy.md)** <br/> |Adds a new Visio Services application proxy to a farm.  <br/> |
|**[Remove-SPVisioSafeDataProvider](remove-spvisiosafedataprovider.md)** <br/> |Removes a data provider from a Visio Services application.  <br/> |
|**[Set-SPVisioExternalData](set-spvisioexternaldata.md)** <br/> |Configures settings related to external data connections for a Visio Services application.  <br/> |
|**[Set-SPVisioPerformance](set-spvisioperformance.md)** <br/> |Sets performance properties for a Visio Services application.  <br/> |
|**[Set-SPVisioSafeDataProvider](set-spvisiosafedataprovider.md)** <br/> |Specifies a description of a safe data provider for a Visio Services application.  <br/> |
|**[Set-SPVisioServiceApplication](set-spvisioserviceapplication.md)** <br/> |Sets the **ServiceApplicationPool** property for a Visio Services application.  <br/> |
   
## See also

#### 

[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md)

