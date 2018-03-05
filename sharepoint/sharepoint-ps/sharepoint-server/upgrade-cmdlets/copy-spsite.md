---
title: "Copy-SPSite"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ebf6155a-4213-481a-ac31-99ea0a095924

description: "Makes a copy of a site collection."
---

# Copy-SPSite

Makes a copy of a site collection.
  
```
Copy-SPSite -Identity <SPSitePipeBind> -TargetUrl <String> [-AssignmentCollection <SPAssignmentCollection>] [-DestinationDatabase <SPContentDatabasePipeBind>] [-HostHeaderWebApplication <String>] [-PreserveSiteId <SwitchParameter>]

```

## Example

--------------EXAMPLE-------------
  
```
Copy-SPSite http://contoso/sites/OldTeam -DestinationDatabase WSS_Content -TargetUrl http://contoso/sites/NewTeam
```

This example makes a copy of the http://contoso/sites/OldTeam site collection from its database to the WSS_Content database with the new URL, http://contoso/sites/NewTeam and a new Site ID.
  
## Detailed Description

Use the **Copy-SPSite** cmdlet to make a copy of a site collection from an implied source content database to a specified destination content database. 
  
The copy of the site collection has a new URL and a new SiteID. When you have database snapshot capabilities on a computer running SQL Server, a temporary snapshot of the source database is created for the duration of the copy to prevent any data changes during the copy process. If you do not have database snapshot capabilities on the server running SQL Server, you can back up the source and restore it to the destination to get the same result.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the site collection to copy. This can be a valid URL or GUID.  <br/> |
| _TargetUrl_ <br/> |Required  <br/> |System.String  <br/> |The URL that will be used for the destination copy of the site collection.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _DestinationDatabase_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the location where the copy will be sent to.  <br/> |
| _HostHeaderWebApplication_ <br/> |Optional  <br/> |System.String  <br/> |Use when the site collection is a host header named site collection that allows the site to land on the correct web application.  <br/> |
| _PreserveSiteId_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies if the SiteID is to be saved or not.  <br/> The valid values are **True** and **False**. The default value is **False**.  <br/> |
   
## See also

#### 

[Test-SPSite](test-spsite.md)
  
[Repair-SPSite](repair-spsite.md)

