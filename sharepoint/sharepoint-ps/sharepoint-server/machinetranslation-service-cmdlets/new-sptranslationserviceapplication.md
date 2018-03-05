---
title: "New-SPTranslationServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa838029-e6e3-4551-9fc3-1c3c4f596e0a

description: "Provisions a new instance of the Machine Translation service."
---

# New-SPTranslationServiceApplication

Provisions a new instance of the Machine Translation service.
  
```
New-SPTranslationServiceApplication -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> -Name <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DatabaseCredential <PSCredential>] [-DatabaseName <String>] [-DatabaseServer <String>] [-Default <SwitchParameter>] [-DeferUpgradeActions <SwitchParameter>] [-FailoverDatabaseServer <String>] [-PartitionMode <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

-------------EXAMPLE---------------
  
```
New-SPTranslationServiceApplication -Name TranslationService -ApplicationPool "SharePoint Web Services Default" -DatabaseServer Server1 -DatabaseName TranslationServiceDatabase
```

This example creates a Machine Translation service application named TranslationService which will run in the SharePoint Web Services Default service application pool. The database will be called TranslationServiceDatabase and will be hosted on the Server1 SQL server instance.
  
## Detailed Description

Use the **New-SPTranslationServiceApplication** cmdlet to provision a new instance of the Machine Translation service on the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ApplicationPool_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the managed application pool that the instance of Translation Service will run in.  <br/> |
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the unique identifier of Translation Service instance to be created.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseCredential_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the SQL Server credentials used for this Translation Service instance. This parameter to be used only used for SQL authentication; if not present, Windows authentication is used instead.  <br/> |
| _DatabaseName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the database name which is to be used for this Translation Service instance.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the database server which is to be used for this Translation Service instance.  <br/> |
| _Default_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Determines whether or not the proxy for this service application should be added to the default proxy group for this Web application.  <br/> |
| _DeferUpgradeActions_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |PARAMVALUE: SwitchParameter  <br/> |
| _FailoverDatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the SQL server instance that will be used as a backup to the primary SQL Server instance.  <br/> |
| _PartitionMode_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Restricts this service to behave uniquely on a partitioned set of site collections. This cannot be changed after the application is provisioned  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseCredential** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**Default** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Set-SPTranslationServiceApplication](set-sptranslationserviceapplication.md)
  
[New-SPTranslationServiceApplicationProxy](new-sptranslationserviceapplicationproxy.md)
  
[Set-SPTranslationServiceApplicationProxy](set-sptranslationserviceapplicationproxy.md)

