---
title: "Restore-SPEnterpriseSearchServiceApplication"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 2/11/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fb717b7b-53cd-44c4-b94d-348c6403d4b2

description: "Restores third-party backup of a search application."
---

# Restore-SPEnterpriseSearchServiceApplication

Restores third-party backup of a search application.
  
```
Restore-SPEnterpriseSearchServiceApplication -AdminSearchServiceInstance <SearchServiceInstancePipeBind> -DatabaseName <String> -DatabaseServer <String> [-DatabasePassword <SecureString>] [-DatabaseUsername <String>] [-FailoverDatabaseServer <String>] <COMMON PARAMETERS>

```

## Example

-------------EXAMPLE 1--------------
  
```
$searchInstance = Get-SPEnterpriseSearchServiceInstance -local
$applicationPool = New-SPServiceApplicationPool -Name "SearchServiceApplicationPool" -Account "domain\username"
Restore-SPEnterpriseSearchServiceApplication -Name "SearchServiceApplication" -ApplicationPool $applicationPool -AdminSearchServiceInstance $searchInstance -DatabaseName "SearchServiceApplication_Admindb" -DatabaseServer "SQLServer1"
```

This example uses Application Configuration Attach mode to restore configuration data.
  
-------------EXAMPLE 2--------------
  
```
$applicationPool = New-SPServiceApplicationPool -Name "SearchServiceApplicationPool" -Account "domain\username"
Restore-SPEnterpriseSearchServiceApplication -Name "SearchServiceApplication" -ApplicationPool $applicationPool -TopologyFile "C:\TopologyFile.xml"
```

This example uses Search Application Attach mode to restore topology data in the file that is named  `topology.xml`.
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
This cmdlet is used by third parties to create a search application that uses existing data.
  
Some third parties back up the application data and have to restore the application later. So, the data is restored and uses the **Restore-SPEnterpriseSearchServiceApplication** cmdlet to create a new search application that uses the restored data. 
  
This cmdlet supports parameter sets. The first set of parameters is for Application Configuration Attach mode and the second set of parameters is for Search Application Attach mode.
  
Application Configuration Attach mode only restores configuration data that is stored in the administration database. However, Search Application Attach restores configuration, topology and all crawled data.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AdminSearchServiceInstance_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceInstancePipeBind  <br/> |Specifies the search service instance to be used with the administration component.  <br/> |
| _ApplicationPool_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the application pool for the query web service.  <br/> |
| _DatabaseName_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the database to create for the restoring the search application.  <br/> The type must be a valid name of a SQL Server database, for example, RestoreDB1.  <br/> |
| _DatabaseServer_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the host server for the database specified in **DatabaseName**.  <br/> The type must be a valid SQL Server host name, for example, SQLServerHost1.  <br/> |
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the new Search application name.  <br/> |
| _TopologyFile_ <br/> |Required  <br/> |System.String  <br/> |Specifies the path of the .XML file that contains the application topology information.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabasePassword_ <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the name of the password for the database server on the SQL Server.  <br/> |
| _DatabaseUsername_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the account name that is specified in the **Database Server** parameter.  <br/> |
| _DeferUpgradeActions_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |When specified, application and database upgrade is not triggered after restoring.  <br/> |
| _FailoverDatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Use this parameter if you want the administration database to use a failover database server.  <br/> |
| _KeepId_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies if the search service application ID's from the topology .xml file should be used for the restored search service application.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Parameters

****

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the application pool for the query web service.  <br/> |
|**TopologyFile** <br/> |Required  <br/> |System.String  <br/> |Specifies the path of the .XML file that contains the application topology information.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**AdminSearchServiceInstance** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceInstancePipeBind  <br/> ||
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**DatabaseName** <br/> |Required  <br/> |System.String  <br/> ||
|**DatabaseServer** <br/> |Required  <br/> |System.String  <br/> ||
|**TopologyFile** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabasePassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> ||
|**DatabaseUsername** <br/> |Optional  <br/> |System.String  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**KeepId** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchServiceApplication](get-spenterprisesearchserviceapplication.md)
  
[New-SPEnterpriseSearchServiceApplication](new-spenterprisesearchserviceapplication.md)
  
[Remove-SPEnterpriseSearchServiceApplication](remove-spenterprisesearchserviceapplication.md)
  
[Resume-SPEnterpriseSearchServiceApplication](resume-spenterprisesearchserviceapplication.md)
  
[Set-SPEnterpriseSearchServiceApplication](set-spenterprisesearchserviceapplication.md)
  
[Upgrade-SPEnterpriseSearchServiceApplication](upgrade-spenterprisesearchserviceapplication.md)
  
[Suspend-SPEnterpriseSearchServiceApplication](suspend-spenterprisesearchserviceapplication.md)

