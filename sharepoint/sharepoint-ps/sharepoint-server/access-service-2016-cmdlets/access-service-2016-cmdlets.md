---
title: "Access Service cmdlets in SharePoint Server 2016"
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
ms.assetid: 90833001-76c1-4933-88d2-d258a7921215
description: "Summary: Lists Windows PowerShell cmdlets that help you manage Access Services applications that run in a 2010 SharePoint experience version of a site collection."
---

# Access Service cmdlets in SharePoint Server 2016

 **Summary:** Lists Windows PowerShell cmdlets that help you manage Access Services applications that run in a 2010 SharePoint experience version of a site collection. 
  
Access Services 2010 is a service in SharePoint Server 2016 that lets an administrator view, edit, and configure a Microsoft Access service application that runs in a 2010 SharePoint experience version of a site collection. A site collection that uses the 2010 experience version runs in SharePoint Server 2016, but the user interface and user experience of the site collection is that of SharePoint Server 2010.
  
All Access Services settings support backup and recovery, regardless of whether there is a user interface setting in Central Administration. However, backup and recovery only apply to service-level and administrative-level settings; end-user content from the Access Services application is not backed up as part of this process.
  
Access Services has Microsoft PowerShell functionality that you can use to provision the service or provision a new instance that uses settings from a previous backup; configure and manage macro and query setting; manage and configure session management; and configure all the global settings of the service.
  
[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md) includes a complete list of all cmdlets in SharePoint Server 2016. 
  
|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Get-SPAccessServiceApplication](get-spaccessserviceapplication.md)** <br/> |Returns an Access Services application or a collection of Access Services applications.  <br/> |
|**[New-SPAccessServiceApplication](new-spaccessserviceapplication.md)** <br/> |Creates a new instance of an Access Services application.  <br/> |
|**[Set-SPAccessServiceApplication](set-spaccessserviceapplication.md)** <br/> |Sets global properties of an existing Access Services application.  <br/> |
   
## See also

#### 

[Microsoft PowerShell for SharePoint Server reference](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/microsoft-powershell-for-sharepoint-server-reference.md)

