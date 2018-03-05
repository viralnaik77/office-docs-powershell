---
title: "Set-SPEnterpriseSearchService"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8baccd0-21d2-40aa-b700-997ec7ca7011

description: "Sets the properties of a search service for a farm."
---

# Set-SPEnterpriseSearchService

Sets the properties of a search service for a farm.
  
```
Set-SPEnterpriseSearchService [-AcknowledgementTimeout <String>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-ConnectionTimeout <String>] [-ContactEmail <String>] [-Identity <SearchServicePipeBind>] [-IgnoreSSLWarnings <String>] [-InternetIdentity <String>] [-PerformanceLevel <String>] [-ProxyType <String>] [-ServiceAccount <String>] [-ServicePassword <SecureString>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$password = Read-Host -AsSecureString**********
```

```
Set-SPEnterpriseSearchService -IgnoreSSLWarnings $true -ServiceAccount contoso\adminAccount -ServicePassword $password

```

This example configures the search service to ignore SSL warnings, and changes the service account for the search service.
  
## Detailed Description

This cmdlet updates properties of a search service for a farm.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AcknowledgementTimeout_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the time in seconds that the crawl component will wait for request acknowledgement while connecting to other services.  <br/> The type must be string input that can be parsed to an integer value.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _ConnectionTimeout_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the time in seconds that the crawl component waits while connecting to other services.  <br/> The type must be string input that can be parsed to an integer value.  <br/> |
| _ContactEmail_ <br/> |Optional  <br/> |System.String  <br/> |Specifies an e-mail address to which external site administrators can write if problems occur when the site is being crawled.  <br/> The type must be a valid e-mail address, in the form MyAddress@mycompany.com.  <br/> |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServicePipeBind  <br/> |Specifies the search service to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchService1); or an instance of a valid **SearchService** object.  <br/> |
| _IgnoreSSLWarnings_ <br/> |Optional  <br/> |System.String  <br/> |Specifies that the search service will ignore Secure Sockets Layer (SSL) certificate name warnings. The default value is **False**.  <br/> The type must be a string that can be cast to a Boolean value, for example, **True** or **False**.  <br/> |
| _InternetIdentity_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the value that the crawler sends in the headers of its HTTP requests to sites when it fetches their pages.  <br/> |
| _PerformanceLevel_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the relative number of threads for the crawl component performance.  <br/> The type must be one of the following values: **Reduced**, **PartlyReduced**, or **Maximum**. The default value is **Maximum**.  <br/> **Reduced**: Total number of threads = number of processors, Max Threads/host = number of processors.  <br/> **Partly Reduced**: Total number of threads = 16 times the number of processors , Max Threads/host = 8 plus the number of processors. Threads are assigned **Below Normal** priority.  <br/> **Maximum**: Total number of threads = 32 times the number of processors, Max Threads/host = 8 plus the number of processors. Threads are assigned **Normal** priority.  <br/> |
| _ProxyType_ <br/> |Optional  <br/> |System.String  <br/> |Specifies whether the search service uses a proxy server or connects directly when crawling content. The default value is **Direct**, (No proxy server is used).  <br/> The type must be one of the following values: **Direct** or **Proxy**.  <br/> |
| _ServiceAccount_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the user account or service account to use for running the search service. The type must be a valid account name on the domain, in the form **Domain\user name** or **user name**.  <br/> When this parameter is used, the **ServicePassword** parameter must also be specified.  <br/> > [!NOTE]> After using this cmdlet to change the service account, you must restart the SharePoint Server 2016 Search Host Controller service on servers hosting any of the following search components: the index component, query processing component, search administration component, content processing component, or analytics processing component.           |
| _ServicePassword_ <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the password for the service account specified in **ServiceAccount**.  <br/> The type must contain the domain password to the account specified in the **ServiceAccount** parameter.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServicePipeBind  <br/> ||
|**AcknowledgementTimeout** <br/> |Optional  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ConnectionTimeout** <br/> |Optional  <br/> |System.String  <br/> ||
|**ContactEmail** <br/> |Optional  <br/> |System.String  <br/> ||
|**IgnoreSSLWarnings** <br/> |Optional  <br/> |System.String  <br/> ||
|**InternetIdentity** <br/> |Optional  <br/> |System.String  <br/> ||
|**PerformanceLevel** <br/> |Optional  <br/> |System.String  <br/> ||
|**ProxyType** <br/> |Optional  <br/> |System.String  <br/> ||
|**ServiceAccount** <br/> |Optional  <br/> |System.String  <br/> ||
|**ServicePassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchService](get-spenterprisesearchservice.md)

