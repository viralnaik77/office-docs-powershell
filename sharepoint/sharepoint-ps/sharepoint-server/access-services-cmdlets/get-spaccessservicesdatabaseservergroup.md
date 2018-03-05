---
title: "Get-SPAccessServicesDatabaseServerGroup"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/20/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a8c1d550-1a00-47dc-a31d-7833b7ab0f05

description: "Returns the settings for all application server groups."
---

# Get-SPAccessServicesDatabaseServerGroup

Returns the settings for all application server groups.
  
```
Get-SPAccessServicesDatabaseServerGroup [-ServiceContext] <SPServiceContextPipeBind> [[-DatabaseServerGroup] <AccessServicesDatabaseServerGroupPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Get-SPAccessServicesDatabaseServerGroup** cmdlet to display the settings for all application server groups using the Access Services 2013 service. If the database server group is not specified, the cmdlet returns the collection of Access Services database server groups that are in the Web service Application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the Access service application.  <br/> |
|**DatabaseServerGroup** <br/> |Optional  <br/> |Microsoft.Office.Access.Services.PowerShell.AccessServicesDatabaseServerGroupPipeBind  <br/> |Specifies the Access application server.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## Example

-------------EXAMPLE-------
  
```
$ASapp = Get-SPAccessServicesApplication
```

```
$app = $Null
```

```
if ($ASapp.length -ne $Null) { $app = $ASapp[0] } else { $app = $ASapp }
```

```
$context = [Microsoft.SharePoint.SPServiceContext]::GetContext($app.ServiceApplicationProxyGroup, [Microsoft.SharePoint.SPSiteSubscriptionIdentifier]::Default)
```

```
$dsg = Get-SPAccessServicesDatabaseServerGroup -ServiceContext $context
```

This example returns all Access Services database server group from the farm.
  
## See also

#### 

[Set-SPAccessServicesDatabaseServerGroupMapping](set-spaccessservicesdatabaseservergroupmapping.md)

