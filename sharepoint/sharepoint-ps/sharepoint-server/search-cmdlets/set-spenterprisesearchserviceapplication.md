---
title: "Set-SPEnterpriseSearchServiceApplication"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77868ee0-716d-48a4-81dc-016b28652710

description: "Sets the properties of a search service application for a farm."
---

# Set-SPEnterpriseSearchServiceApplication

Sets the properties of a search service application for a farm.
  
```
Set-SPEnterpriseSearchServiceApplication -Identity <SearchServiceApplicationPipeBind> [-AdminApplicationPool <SPIisWebServiceApplicationPoolPipeBind>] [-ApplicationPool <SPIisWebServiceApplicationPoolPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DatabaseName <String>] [-DatabasePassword <SecureString>] [-DatabaseServer <String>] [-DatabaseUsername <String>] [-DefaultContentAccessAccountName <String>] [-DefaultContentAccessAccountPassword <SecureString>] [-DefaultSearchProvider <Default | SharepointSearch | FASTSearch>] [-DiacriticSensitive <String>] [-FailoverDatabaseServer <String>] [-VerboseQueryMonitoring <String>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
Set-SPEnterpriseSearchServiceApplication -Identity "Search Service Application" -VerboseQueryMonitoring True
```

This example turns on verbose query logging in the default search service application named  `Search Service Application`.
  
## Detailed Description

This cmdlet updates properties of a search service application. **SPEnterpriseSearchServiceApplication** represents a self-contained aggregation of indexed content and properties available for search, and provides an anchor class for setting global search properties. A search application can include multiple search service applications. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search service application to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a search service application (for example, MySearchApp); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AdminApplicationPool_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the application pool for the administrative web service for the search service application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an application pool (for example, AdminAppPool1); or an instance of a valid **IISWebServiceApplicationPool** object.  <br/> |
| _ApplicationPool_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies an application pool for the search service application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an application pool (for example, AppPool1); or an instance of a valid **IISWebServiceApplicationPool** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the database for the Web service administration.  <br/> The type must be a valid name of a SQL Server database, for example WebAdminDB1.  <br/> |
| _DatabasePassword_ <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the password for the user ID that is used for accessing the web service administration database on SQL Server.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the web service administration database.  <br/> The type must be a valid SQL Server host name, for example, SQLServerHost1.  <br/> |
| _DatabaseUsername_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the user ID to use for accessing the web service administration database.  <br/> The type must be a valid user name, for example, WebAdminUserDB1.  <br/> |
| _DefaultContentAccessAccountName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the account ID to use for accessing content.  <br/> The type must be a valid user name, for example, ContentAccessUser1.  <br/> |
| _DefaultContentAccessAccountPassword_ <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the password for the content access account.  <br/> The type must be a valid password.  <br/> |
| _DefaultSearchProvider_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Query.SearchProvider  <br/> |Specifies the search application type to be used for this application. This parameter has been deprecated for SharePoint Server 2016.  <br/> |
| _DiacriticSensitive_ <br/> |Optional  <br/> |System.String  <br/> |Specifies that the search application respects diacritics (for example, ä). The default value is **false**.  <br/> |
| _FailoverDatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host SQL instance for the failover database server.  <br/> The type must be a valid SQL Server instance name, for example, SQLServerHost1.  <br/> |
| _VerboseQueryMonitoring_ <br/> |Optional  <br/> |System.String  <br/> |Enables verbose query logging. The default value is **False**.  <br/> The type must be a string that can be cast to a Boolean value, for example, **True** or **False**.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AdminApplicationPool** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**ApplicationPool** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabasePassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseUsername** <br/> |Optional  <br/> |System.String  <br/> ||
|**DefaultContentAccessAccountName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DefaultContentAccessAccountPassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> ||
|**DefaultSearchProvider** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**DiacriticSensitive** <br/> |Optional  <br/> |System.String  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**VerboseQueryMonitoring** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchServiceApplication](new-spenterprisesearchserviceapplication.md)
  
[Get-SPEnterpriseSearchServiceApplication](get-spenterprisesearchserviceapplication.md)
  
[Remove-SPEnterpriseSearchServiceApplication](remove-spenterprisesearchserviceapplication.md)
  
[Restore-SPEnterpriseSearchServiceApplication](restore-spenterprisesearchserviceapplication.md)
  
[Upgrade-SPEnterpriseSearchServiceApplication](upgrade-spenterprisesearchserviceapplication.md)
  
[Suspend-SPEnterpriseSearchServiceApplication](suspend-spenterprisesearchserviceapplication.md)
  
[Resume-SPEnterpriseSearchServiceApplication](resume-spenterprisesearchserviceapplication.md)

