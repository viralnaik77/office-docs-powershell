---
title: "Test-SPContentDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ed095a0a-fa1a-4323-8503-624f0e09707d

description: "Tests a content database."
---

# Test-SPContentDatabase

Tests a content database.
  
```
Test-SPContentDatabase [-Identity] <SPContentDatabasePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-DatabaseCredentials <PSCredential>] [-ExtendedCheck <SwitchParameter>] [-ServerInstance <SPDatabaseServiceInstancePipeBind>] [-ShowLocation <SwitchParameter>] [-ShowRowCounts <SwitchParameter>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **Test-SPContentDatabase** cmdlet to test a content database against a Web application to verify all customizations referenced within the content database are also installed in the web application. This cmdlet can be issued against a content database currently attached to the farm, or a content database that is not connected to the farm. It can be used to test content databases from SharePoint Server 2016. 
  
> [!NOTE]
> The **Test-SPContentDatabase** cmdlet does not change any of the data or structure of the content database, but can cause load on the database while the checks are in progress, which could temporarily block use of the content database. This cmdlet should only be used against a content database that is currently under low or no usage. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies an existing connected SharePoint Server 2016 content database to one of the two parameter sets in the form of a GUID or database name if it is unique.  <br/> |
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the existing content database to test.  <br/> The type must be a valid name of a SharePoint content database; for example, SPContentDB1.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the SharePoint Web application to use to test the content database.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of SharePoint Web application (for example, MyOfficeApp1); or an instance of a valid **SPWebApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the **PSCredential** object that contains the user name and password to be used for database SQL Server Authentication.  <br/> The type must be a valid **PSCredential** object.  <br/> |
|**ExtendedCheck** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Checks for inconsistent authentication modes during database-attach upgrade process.  <br/> The selected mode, claims or classic, must be the same in both versions.  <br/> |
|**ServerInstance** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPDatabaseServiceInstancePipeBind  <br/> |Specifies the instance of the database service to use to test the specified content database.  <br/> The type must be a valid GUID, such as 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SQL Server instance (for example, DBSvrInstance1); or an instance of a valid **SPDatabaseServiceInstance** object.  <br/> |
|**ShowLocation** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies the locations where missing templates and features are being used within the database. Typically, reported locations are scoped within the site collections that are within the specified content database.  <br/> > [!NOTE]> The use of the parameter significantly increases the time to complete the test procedure.           |
|**ShowRowCounts** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Returns database statistics which are row counts for tables in the content database.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**ExtendedCheck** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ServerInstance** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPDatabaseServiceInstancePipeBind  <br/> ||
|**ShowLocation** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ShowRowCounts** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

----------------------------EXAMPLE 1-----------------------
  
```
Test-SPContentDatabase -name WSS_Content_DB -webapplication http://sitename
```

This example tests the  `WSS_Content_DB` content database against the  `sitename` Web application, and returns a list of issues. 
  
----------------------------EXAMPLE 2-----------------------
  
```
$DB = Get-SPContentDatabase -site http://contoso.com
```

```
Test-SPContentDatabase $DB -showrowcounts
```

This example gets the content database that contains the site collection at  `http://contoso.com`, and then tests the database against the Web application that hosts it to determine issues. Together with displaying the list of issues, by specifying the **ShowRowCounts** parameter, this also returns the table size metrics from the content database. 
  
## See also

#### 

[Get-SPContentDatabase](get-spcontentdatabase.md)
  
[Set-SPContentDatabase](set-spcontentdatabase.md)
  
[Mount-SPContentDatabase](mount-spcontentdatabase.md)
  
[Upgrade-SPContentDatabase](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/upgrade-cmdlets/upgrade-spcontentdatabase.md)
#### 

[New-SPContentDatabase](http://technet.microsoft.com/library/18cf18cd-8fb7-4561-be71-41c767f27b51.aspx)
  
[Remove-SPContentDatabase](http://technet.microsoft.com/library/e8c337b6-37af-4fdd-8469-a32f4d45c040.aspx)

