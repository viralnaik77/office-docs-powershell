---
title: "Copy-SPAccessServicesDatabaseCredentials"
ms.author: kirks
author: Techwriter40
ms.date: 10/20/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83e8dd77-fcfb-4213-98ce-2b8512d0d911

description: "Copies credentials of an application from one logical server to another."
---

# Copy-SPAccessServicesDatabaseCredentials

Copies credentials of an application from one logical server to another.
  
```
Copy-SPAccessServicesDatabaseCredentials -AppUrl <String> -ServerCredential <NetworkCredential> -ServiceContext <SPServiceContextPipeBind> -SourceServer <String> -TargetServer <String> [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

------------EXAMPLE 1------------------
  
```
$appUrl = $app.Url.OriginalString
```

```
$web = Get-SPWeb $appUrl
```

```
$site = $web.Site
```

```
$serviceContext = [Microsoft.Sharepoint.SPServiceContext]::GetContext($serviceApp.ServiceApplicationProxyGroup, $site.SiteSubscription.Id);
```

```
$serverCredential = Get-CredentialFromSecretsHashWithFarmId -Hash $Secrets -Type $SqlAzureServerPasswordGridSecretType -FarmId $SourceSqlFarm
```

```
$sourceServerFQDN = $sourceDatabaseHost.Server + "." + $sourceDatabaseHost.Domain
```

```
$targetServerFQDN = $targetDatabaseHost.Server + "." + $targetDatabaseHost.Domain
```

```
Copy-SPAccessServicesDatabaseCredentials -ServiceContext $serviceContext -AppUrl $appUrl -SourceServer $sourceServerFQDN -TargetServer $targetServerFQDN -ServerCredential $serverCredential
```

This example copies credentials from a source to a target.
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AppUrl_ <br/> |Required  <br/> |System.String  <br/> |Specifies the URL of the current application.  <br/> |
| _ServerCredential_ <br/> |Required  <br/> |System.Net.NetworkCredential  <br/> |Specifies the network credentials used to access the current application.  <br/> |
| _ServiceContext_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Represents the context object that encapsulates all the information that is required to make a call to a service application.  <br/> |
| _SourceServer_ <br/> |Required  <br/> |System.String  <br/> |Specifies the fully qualified name of the current server.  <br/> |
| _TargetServer_ <br/> |Required  <br/> |System.String  <br/> |Specifies the fully qualified name of the new server.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   

