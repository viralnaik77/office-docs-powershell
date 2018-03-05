---
title: "New-SPEnterpriseSearchServiceApplication"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 2/11/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3360bbb7-394d-4b13-bf86-e9cd7caa43ba

description: "Adds a search service application to a farm."
---

# New-SPEnterpriseSearchServiceApplication

Adds a search service application to a farm.
  
```
New-SPEnterpriseSearchServiceApplication -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> [-AdminApplicationPool <SPIisWebServiceApplicationPoolPipeBind>] [-CloudIndex <$true | $false>] [-DatabaseName <String>] [-DatabasePassword <SecureString>] [-DatabaseServer <String>] [-DatabaseUsername <String>] [-FailoverDatabaseServer <String>] [-Name <String>] [-Partitioned <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$appPool = New-SPServiceApplicationPool -name "SsaAppPool" -account contoso\adminUser
$ssa = New-SPEnterpriseSearchServiceApplication -Name "NewSSA" -ApplicationPool $appPool
```

This example creates a new search service application named  `NewSSA` in a new application pool. A search service application that is created in this manner will have active search topology, but no search components. 
  
## Detailed Description

This cmdlet is used when the search functionality is first configured or when a new shared search application is added to a farm. **SPEnterpriseSearchServiceApplication** represents a self-contained aggregation of indexed content and properties available for search, and provides an anchor class for setting global search properties. A farm can include multiple search service applications. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ApplicationPool_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the IIS application pool to use for the new search application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL of a search application, in the form http://server_name; or an instance of a valid **SPIisWebServiceApplicationPool** object.  <br/> |
| _AdminApplicationPool_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the application pool to be used with the SearchAdminWebServiceApplication that is associated with SearchServiceApplication. If not specified, **ApplicationPool** will be used.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CloudIndex_ <br/> |Optional  <br/> |System.Boolean  <br/> |When **CloudIndex** is true, this becomes a cloud Search service application that crawls on premises content in a cloud hybrid search solution.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the database to create for the new search application.  <br/> The type must be a valid name of a SQL Server database, for example, SearchAppDB1.  <br/> |
| _DatabasePassword_ <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the password for the user ID that is used for accessing the search application database on SQL Server.  <br/> The type must be a valid password.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the database specified in **DatabaseName**.  <br/> The type must be a valid SQL Server host name, for example, SQLServerHost1.  <br/> |
| _DatabaseUsername_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the user ID to use for accessing the search application SQL Server database.  <br/> The type must be a valid user name, for example, SearchUserName1.  <br/> |
| _FailoverDatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the SQL server that hosts the mirror instances of search databases.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the names of the new search application.  <br/> The type must be a valid name of a search application, for example, SearchApp1.  <br/> |
| _Partitioned_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the search service application uses web-hosted mode. web-hosted mode segregates results for a given hosted subscription.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**AdminApplicationPool** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabasePassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseUsername** <br/> |Optional  <br/> |System.String  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**Partitioned** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchServiceApplication](get-spenterprisesearchserviceapplication.md)
  
[Set-SPEnterpriseSearchServiceApplication](set-spenterprisesearchserviceapplication.md)
  
[Remove-SPEnterpriseSearchServiceApplication](remove-spenterprisesearchserviceapplication.md)
  
[Restore-SPEnterpriseSearchServiceApplication](restore-spenterprisesearchserviceapplication.md)
  
[Upgrade-SPEnterpriseSearchServiceApplication](upgrade-spenterprisesearchserviceapplication.md)
  
[Suspend-SPEnterpriseSearchServiceApplication](suspend-spenterprisesearchserviceapplication.md)
  
[Resume-SPEnterpriseSearchServiceApplication](resume-spenterprisesearchserviceapplication.md)

