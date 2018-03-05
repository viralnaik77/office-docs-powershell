---
title: "State service and session state cmdlets in SharePoint Server 2016"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 2/29/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: 353fd164-d9b9-4158-942e-d2725d4e8007
description: "Summary: Lists Windows PowerShell cmdlets that are used to support session state and the state service in SharePoint Server 2016."
---

# State service and session state cmdlets in SharePoint Server 2016

 **Summary:** Lists Windows PowerShell cmdlets that are used to support session state and the state service in SharePoint Server 2016. 
  
These Microsoft PowerShell cmdlets are used to support session state and the state service.
  
[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md) includes a complete list of all cmdlets in SharePoint Server 2016. 
  
|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Disable-SPSessionStateService](disable-spsessionstateservice.md)** <br/> |Turns off the session state service on the farm  <br/> |
|**[Dismount-SPStateServiceDatabase](dismount-spstateservicedatabase.md)** <br/> |Removes the association to a state service database from the farm without dropping the database in the Microsoft SQL Server database  <br/> |
|**[Enable-SPSessionStateService](enable-spsessionstateservice.md)** <br/> |Creates a session state database and turns on the session state service  <br/> |
|**[Get-SPSessionStateService](get-spsessionstateservice.md)** <br/> |Returns the properties of the session state service, including time-out and database settings  <br/> |
|**[Get-SPStateServiceApplication](get-spstateserviceapplication.md)** <br/> |Returns state service applications on the farm  <br/> |
|**[Get-SPStateServiceApplicationProxy](get-spstateserviceapplicationproxy.md)** <br/> |Returns state service application proxies on the farm.  <br/> |
|**[Get-SPStateServiceDatabase](get-spstateservicedatabase.md)** <br/> |Returns a state service database.  <br/> |
|**[Initialize-SPStateServiceDatabase](initialize-spstateservicedatabase.md)** <br/> |Installs the state database schema into a state service database  <br/> |
|**[Mount-SPStateServiceDatabase](mount-spstateservicedatabase.md)** <br/> |Attaches an existing state service database to the farm  <br/> |
|**[New-SPStateServiceApplication](new-spstateserviceapplication.md)** <br/> |Creates a new state service application  <br/> |
|**[New-SPStateServiceApplicationProxy](new-spstateserviceapplicationproxy.md)** <br/> |Creates a proxy for a state service application  <br/> |
|**[New-SPStateServiceDatabase](new-spstateservicedatabase.md)** <br/> |Creates and provisions a new state service database, and installs the state database schema into it  <br/> |
|**[Remove-SPStateServiceDatabase](remove-spstateservicedatabase.md)** <br/> |Removes a state service database from a state service application and drops it from the SQL Server  <br/> |
|**[Resume-SPStateServiceDatabase](resume-spstateservicedatabase.md)** <br/> |Resumes a paused state service database so that new rows of data are received  <br/> |
|**[Set-SPSessionStateService](set-spsessionstateservice.md)** <br/> |Updates the credentials that are used to communicate with the state service database  <br/> |
|**[Set-SPStateServiceApplication](set-spstateserviceapplication.md)** <br/> |Updates the name of a state service application  <br/> |
|**[Set-SPStateServiceApplicationProxy](set-spstateserviceapplicationproxy.md)** <br/> |Updates the name of a state service application proxy  <br/> |
|**[Set-SPStateServiceDatabase](set-spstateservicedatabase.md)** <br/> |Updates properties of a state service database  <br/> |
|**[Suspend-SPStateServiceDatabase](suspend-spstateservicedatabase.md)** <br/> |Pauses a state database and thus prevents new rows of data from being added to a database  <br/> |
   
## See also

#### 

[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md)

