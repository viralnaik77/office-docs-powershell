---
title: "Use Windows PowerShell cmdlets to manage Access Services in SharePoint Server 2016"
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
ms.assetid: 5789d7ec-8216-45f0-8720-32be4df1afba

description: "Summary: Learn about the Microsoft PowerShell cmdlets that you can use to manage Microsoft Access service applications in SharePoint Server 2016."
---

# Use Windows PowerShell cmdlets to manage Access Services in SharePoint Server 2016

 **Summary:** Learn about the Microsoft PowerShell cmdlets that you can use to manage Microsoft Access service applications in SharePoint Server 2016. 


  
Access Services is a service in SharePoint Server 2016 that lets an administrator view, edit, and configure a Microsoft Access service application within a Web browser. 
  
All Access Services settings support backup and recovery, regardless of whether there is a UI setting in Central Administration. However, backup and recovery only apply to service-level and administrative-level settings; end-user content from the Access application is not backed up as part of this process.
  
Access Services has PowerShell functionality that you can use to provision the service or provision a new instance that uses settings from a previous backup; configure and manage macro and query setting; manage and configure session management; and configure all the global settings of the service.
  
Cmdlets that have an ![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png) icon next to them are new cmdlets in SharePoint Server 2016. 
  
[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md) includes a complete list of all cmdlets in SharePoint Server 2016. 
  
|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Copy-SPAccessServicesDatabaseCredentials](copy-spaccessservicesdatabasecredentials.md)          ![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)                             ** <br/> |Copies credentials of an application from one logical server to another.  <br/> |
|**[Export-SPAccessServicesDatabase](export-spaccessservicesdatabase.md)          ![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)                             ** <br/> |Exports the Access Database into a Bacpac package.  <br/> |
|**[Get-SPAccessServicesApplication](get-spaccessservicesapplication.md)** <br/> |Returns an Access Services application or a collection of Access Services applications.  <br/> |
|**[Get-SPAccessServicesDatabase](get-spaccessservicesdatabase.md)** <br/> |Returns an Access Services database or a collection of Access Services databases.  <br/> |
|**[Get-SPAccessServicesDatabaseServer](get-spaccessservicesdatabaseserver.md)** <br/> |Returns the settings for all application servers.  <br/> |
|**[Get-SPAccessServicesDatabaseServerGroup](get-spaccessservicesdatabaseservergroup.md)** <br/> |Returns the settings for all application server groups.  <br/> |
|**[Get-SPAccessServicesDatabaseServerGroupMapping](get-spaccessservicesdatabaseservergroupmapping.md)** <br/> |Returns the mapping from a source package type to the database server group.  <br/> |
|**[Import-SPAccessServicesDatabase](import-spaccessservicesdatabase.md)          ![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)                             ** <br/> |Imports the Access Database from a Bacpac package.  <br/> |
|**[New-SPAccessServicesApplication](new-spaccessservicesapplication.md)** <br/> |Creates a new instance of an Access Services application in SharePoint Server 2016.  <br/> |
|**[New-SPAccessServicesApplicationProxy](new-spaccessservicesapplicationproxy.md)          ![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)                             ** <br/> |Enables the creation of a new proxy for a target Access Services Application.  <br/> |
|**[New-SPAccessServicesDatabaseServer](new-spaccessservicesdatabaseserver.md)** <br/> |Adds a new SQL Server database to the list of servers.  <br/> |
|**[Remove-SPAccessServicesDatabaseServer](remove-spaccessservicesdatabaseserver.md)** <br/> |Removes the specified database server.  <br/> |
|**[Reset-SPAccessServicesDatabasePassword](reset-spaccessservicesdatabasepassword.md)** <br/> |Resets the passwords for all logons for user application databases.  <br/> |
|**[Set-SPAccessServicesApplication](set-spaccessservicesapplication.md)** <br/> |Sets global properties of an existing Access Services application in SharePoint Server 2016.  <br/> |
|**[Set-SPAccessServicesDatabaseServer](set-spaccessservicesdatabaseserver.md)** <br/> |Specifies whether or not a database in SQL Server is available.  <br/> |
|**[Set-SPAccessServicesDatabaseServerGroupMapping](set-spaccessservicesdatabaseservergroupmapping.md)** <br/> |Sets server group mappings.  <br/> |
   
## See also

#### 

[Microsoft PowerShell for SharePoint Server reference](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/microsoft-powershell-for-sharepoint-server-reference.md)

