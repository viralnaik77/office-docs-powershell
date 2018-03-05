---
title: "New-SPSecureStoreServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 57dc65e4-a368-46d4-836d-9850d1215b4b

description: "Creates a new Secure Store Service application proxy in the farm."
---

# New-SPSecureStoreServiceApplicationProxy

Creates a new Secure Store Service application proxy in the farm.
  
```
New-SPSecureStoreServiceApplicationProxy -Uri <Uri> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DefaultProxyGroup <SwitchParameter>] [-Name <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **New-SPSecureStoreServiceApplicationProxy** cmdlet creates a new Secure Store Service application proxy for a Secure Store Service application in the farm. 
  
The **New-SPSecureStoreServiceApplicationProxy** cmdlet does not specify whether the service application proxy is partitioned or not. If you want to specify a partitioned service application proxy, a partitioned service application can be created by using the [New-SPSecureStoreServiceApplication](new-spsecurestoreserviceapplication.md) cmdlet. The result of the **New-SPSecureStoreServiceApplication** cmdlet can be passed to the **New-SPSecureStoreServiceApplicationProxy** cmdlet. Similarly, if you want to specify an unpartitioned service application proxy, an unpartitioned service application can be created by using the [New-SPSecureStoreServiceApplication](new-spsecurestoreserviceapplication.md) cmdlet. The result of the **New-SPSecureStoreServiceApplication** cmdlet can be passed to the **New-SPSecureStoreServiceApplicationProxy** cmdlet. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> |Specifies the local Secure Store Service application associated with the new proxy.  <br/> |
|**Uri** <br/> |Required  <br/> |System.Uri  <br/> |Specifies the URI of a remote Secure Store Service application associated with the new proxy.  <br/> The type must be a valid URI, in the form file:\\server_name\sitedocs.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the service application proxy be added to the farm's default proxy group.  <br/> |
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the new service application proxy to create.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**Uri** <br/> |Required  <br/> |System.Uri  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Errors

|**Error**|**Description**|
|:-----|:-----|
|||
   
## Exceptions

|**Exceptions**|**Description**|
|:-----|:-----|
|||
   
## Example

------------------EXAMPLE 1------------------
  
```
New-SPSecureStoreServiceApplicationProxy -Name "Contoso Service Application Proxy" -ServiceApplication $SSServiceApp
```

This example creates a new Secure Store Service application proxy with the name  `Contoso Service Application Proxy` for the given service application. 
  
------------------EXAMPLE 2------------------
  
```
$nameofproxy = "Connection to: HostedSecureStoreInParentFarm"
```

```
$proxy = Get-SPServiceApplicationProxy | where {$_ -match $nameofproxy}
```

```
$prop = $proxy.Properties
```

```
$type = $prop["Microsoft.Office.Server.Utilities.SPPartitionOptions"].GetType()
```

```
$partition = [enum]::Parse( $type, 1 )
```

```
$prop["Microsoft.Office.Server.Utilities.SPPartitionOptions"] = $partition
```

```
$proxy.Update()
```

This example converts an unpartitioned secure store service application proxy in the child to a partitioned one.
  
## See also

#### 

[New-SPSecureStoreServiceApplication](new-spsecurestoreserviceapplication.md)
  
[Set-SPSecureStoreServiceApplication](set-spsecurestoreserviceapplication.md)

