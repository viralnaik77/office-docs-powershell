---
title: "Get-SPAccessServicesDatabaseServer"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a1aa90e1-04b6-4e4b-8237-74876c4c6507

description: "Returns the settings for all application servers."
---

# Get-SPAccessServicesDatabaseServer

Returns the settings for all application servers.
  
```
Get-SPAccessServicesDatabaseServer [-ServiceContext] <SPServiceContextPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-DatabaseServerGroup <AccessServicesDatabaseServerGroupPipeBind>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **Get-SPAccessServicesDatabaseServer** cmdlet to return the settings for all application servers that use the Access Services 2013 service. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context for the database server.  <br/> |
|**DatabaseServer** <br/> |Required  <br/> |Microsoft.Office.Access.Services.PowerShell.AccessServicesDatabaseServerPipeBind  <br/> |Specifies the database server to return.  <br/> |
|**DatabaseServerGroup** <br/> |Required  <br/> |Microsoft.Office.Access.Services.PowerShell.AccessServicesDatabaseServerGroupPipeBind  <br/> |Specifies the database server group to return.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**DatabaseServer** <br/> |Required  <br/> |Microsoft.Office.Access.Services.PowerShell.AccessServicesDatabaseServerPipeBind  <br/> ||
|**DatabaseServerGroup** <br/> |Required  <br/> |Microsoft.Office.Access.Services.PowerShell.AccessServicesDatabaseServerGroupPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------EXAMPLE--------
  
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
$server2 = $Null
```

```
$getservers = Get-SPAccessServicesDatabaseServer $context
```

This example returns all Access Services databases from the farm.
  
## See also

#### 

[New-SPAccessServicesDatabaseServer](new-spaccessservicesdatabaseserver.md)
  
[Remove-SPAccessServicesDatabaseServer](remove-spaccessservicesdatabaseserver.md)
  
[Set-SPAccessServicesDatabaseServer](set-spaccessservicesdatabaseserver.md)

