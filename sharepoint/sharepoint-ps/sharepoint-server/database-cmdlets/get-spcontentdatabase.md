---
title: "Get-SPContentDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: a4a83bb0-0bab-4cad-9b59-0fd89a16f57b

description: "Returns one or more content databases."
---

# Get-SPContentDatabase

Returns one or more content databases.
  
```
Get-SPContentDatabase [-Identity <SPContentDatabasePipeBind>] [-NoStatusFilter <SwitchParameter>] <COMMON PARAMETERS>

```

## Example

----------------EXAMPLE 1------------
  
```
Get-SPContentDatabase -webapplication http://sitename
```

This example returns all content databases used by the  `sitename` Web application. 
  
----------------EXAMPLE 2------------
  
```
Get-SPContentDatabase -site http://contoso.com
```

This example returns the content database that contains the site collection at  `http://contoso.com`.
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
The **Get-SPContentDatabase** cmdlet returns the specified content databases. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ConnectAsUnattachedDatabase_ <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that only unattached databases in the farm are returned.  <br/> |
| _DatabaseName_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the database in the farm.  <br/> |
| _DatabaseServer_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the database server in the farm.  <br/> |
| _Site_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Returns the content database for the specified site collection.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL, in the form http://server_name; or an instance of a valid **SPSite** object.  <br/> |
| _WebApplication_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Returns the content databases for the specified Web application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of SharePoint Web application (for example, MyOfficeApp1); or an instance of a valid **SPWebApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _DatabaseCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the **PSCredential** object that contains the user name and password to be used for database SQL Server Authentication.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _Identity_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies a specific content database to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint content database (for example, SPContentDB1); or an instance of a valid **SPContentDatabase** object.  <br/> |
| _NoStatusFilter_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether a status filter is turned on.  <br/> The valid values are **True** or **False**. The default value is **False**.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> ||
|**ConnectAsUnattachedDatabase** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseName** <br/> |Required  <br/> |System.String  <br/> ||
|**DatabaseServer** <br/> |Required  <br/> |System.String  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
   
## See also

#### 

[Set-SPContentDatabase](set-spcontentdatabase.md)
  
[Mount-SPContentDatabase](mount-spcontentdatabase.md)
  
[Test-SPContentDatabase](test-spcontentdatabase.md)
  
[Upgrade-SPContentDatabase](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/upgrade-cmdlets/upgrade-spcontentdatabase.md)
#### 

[New-SPContentDatabase](http://technet.microsoft.com/library/18cf18cd-8fb7-4561-be71-41c767f27b51.aspx)
  
[Remove-SPContentDatabase](http://technet.microsoft.com/library/e8c337b6-37af-4fdd-8469-a32f4d45c040.aspx)

