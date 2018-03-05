---
title: "Set-SPEnterpriseSearchCrawlDatabase"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 2/11/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 013afca3-9aba-47ee-ad44-b20d1dc17f16

description: "Sets properties of a crawl database for a Search service application."
---

# Set-SPEnterpriseSearchCrawlDatabase

Sets properties of a crawl database for a Search service application.
  
```
Set-SPEnterpriseSearchCrawlDatabase -Identity <CrawlStorePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DatabaseName <String>] [-DatabasePassword <SecureString>] [-DatabaseServer <String>] [-DatabaseUsername <String>] [-FailoverDatabaseServer <String>] [-SearchApplication <SearchServiceApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$searchApp = Get-SPEnterpriseSearchServiceApplication mySearchServiceAppSet-SPEnterpriseSearchCrawlDatabase -Identity SearchApp_CrawlStore-SearchApplication $searchApp -FailoverDatabaseServer \\failoverServer
```

This example sets the failover database server for the crawl database,  `SearchApp_CrawlStore`, to the  `\\failoverServer` server. 
  
## Detailed Description

The **Set-SPEnterpriseSearchCrawlDatabase** cmdlet sets properties of a specified crawl database for a Search service application. A crawl database stores crawl history for a Search service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawlStorePipeBind  <br/> |Specifies the crawl database to modify.  <br/> A valid crawl database name, in the form CrawlStore1; or a valid GUID, such as 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid **CrawlStore** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the database to create for the crawl database. The type must be a valid name of a SQL Server database; for example, CrawlStoreDB1.  <br/> |
| _DatabasePassword_ <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the password for the Microsoft SQL Server database server.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the database specified in **DatabaseName**. The type must be a valid SQL Server host name; for example, SQLServerHost1.  <br/> |
| _DatabaseUsername_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the account name on the **Database Server**.  <br/> |
| _FailoverDatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the server to be used for failover when SQL Server mirroring is used.  <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the name of the search application to which the crawl database applies.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawlStorePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabasePassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseUsername** <br/> |Optional  <br/> |System.String  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchCrawlDatabase](get-spenterprisesearchcrawldatabase.md)
  
[New-SPEnterpriseSearchCrawlDatabase](new-spenterprisesearchcrawldatabase.md)
  
[Remove-SPEnterpriseSearchCrawlDatabase](remove-spenterprisesearchcrawldatabase.md)

