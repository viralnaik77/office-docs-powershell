---
title: "New-SPEnterpriseSearchCrawlDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 71a9d57c-4383-497d-8510-9d79c1784a77

description: "Creates a crawl database which can be added to a search service application."
---

# New-SPEnterpriseSearchCrawlDatabase

Creates a crawl database which can be added to a search service application.
  
```
New-SPEnterpriseSearchCrawlDatabase -DatabaseName <String> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DatabasePassword <SecureString>] [-DatabaseServer <String>] [-DatabaseUsername <String>] [-FailoverDatabaseServer <String>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$searchApp = Get-SPEnterpriseSearchServiceApplication mySearchServiceAppNew-SPEnterpriseSearchCrawlDatabase -SearchApplication $searchApp -DatabaseName newCrawlDB
```

This example creates a new crawl database named  `newCrawlDB` for the  `mySearchServiceApp` search service application. 
  
## Detailed Description

The **New-SPEnterpriseSearchCrawlDatabase** cmdlet is used during initial configuration and farm scale-out to create a new crawl database, which can be added to a search service application. A crawl database stores crawl history for a search application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _DatabaseName_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the database to create for the crawl database.  <br/> The type must be a valid name of a SQL Server database; for example, CrawlStoreDB1.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the crawl database.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabasePassword_ <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the name of the password for the Microsoft SQL Server database server.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the database specified in **DatabaseName**.  <br/> The type must be a valid SQL Server host name; for example, SQLServerHost1.  <br/> |
| _DatabaseUsername_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the account name specified in the **Database Server** parameter.  <br/> |
| _FailoverDatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Server that is used for failover when SQL Server mirroring is used.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**DatabaseName** <br/> |Required  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabasePassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseUsername** <br/> |Optional  <br/> |System.String  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Exceptions

|**Exceptions**|**Description**|
|:-----|:-----|
|||
   
## See also

#### 

[Set-SPEnterpriseSearchCrawlDatabase](set-spenterprisesearchcrawldatabase.md)
  
[Get-SPEnterpriseSearchCrawlDatabase](get-spenterprisesearchcrawldatabase.md)
  
[Remove-SPEnterpriseSearchCrawlDatabase](remove-spenterprisesearchcrawldatabase.md)

