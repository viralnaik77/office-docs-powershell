---
title: "New-SPWordConversionServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de13ff64-9d05-408b-a935-528288014d3d

description: "Creates a new instance of a Word Automation Services application on the farm."
---

# New-SPWordConversionServiceApplication

Creates a new instance of a Word Automation Services application on the farm.
  
```
New-SPWordConversionServiceApplication [-Name] <String> -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DatabaseCredential <PSCredential>] [-DatabaseName <String>] [-DatabaseServer <String>] [-Default <SwitchParameter>] [-PartitionMode <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **New-SPWordConversionServiceApplication** cmdlet creates a new instance of a Word Automation Services application on the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the new Word Automation Services application.  <br/> The type must be a valid name of a Word Automation Services application; for example, WordSvcApp1.  <br/> |
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the existing IIS-managed application pool in which this instance of Word Automation Services runs.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an application pool (for example, AppPoolName1); or an instance of a valid **IISWebServiceApplicationPool** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DatabaseCredential** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the credentials to use for connecting to the database for the Word Automation Services application. Use this parameter only if SQL Server Authentication is used to access the service application database.  <br/> When the **DatabaseCredential** parameter is specified, the **DatabaseName** and **DatabaseServer** parameters are required.  <br/> |
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the database to create for the new Word Automation Services application.  <br/> The type must be a valid SQL database name; for example, MetadataDB1.  <br/> |
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the Word Automation Services database.  <br/> The type must be a valid SQL database server host name; for example, SQLServerHost1.  <br/> |
|**Default** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the service application proxy is added to the farm's default proxy group for this Web application.  <br/> |
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that this service behaves uniquely on a partitioned set of site collections. This property cannot be changed after the application is provisioned.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
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
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------EXAMPLE---------------
  
```
Get-SPServiceApplicationPool -Identity MyAppPool | New-SPWordConversionServiceApplication -Name WordServices1
```

This example creates a new Word Automation Services application named  `WordServices1` in an existing application pool named MyAppPool. 
  
## See also

#### 

[Set-SPWordConversionServiceApplication](set-spwordconversionserviceapplication.md)

