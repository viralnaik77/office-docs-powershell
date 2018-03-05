---
title: "Set-SPAppAutoProvisionConnection"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 68bfcaf8-d5f7-43ab-b36d-75128ae28e39

description: "Sets provision connection settings for an app."
---

# Set-SPAppAutoProvisionConnection

Sets provision connection settings for an app.
  
```
Set-SPAppAutoProvisionConnection -ConnectionType <RemoteWebHost> -EndPoint <String> -Password <String> -Username <String> [-AssignmentCollection <SPAssignmentCollection>] [-SiteSubscription <SPSiteSubscriptionPipeBind>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **Set-SPAppAutoProvisionConnection** cmdlet to set provision connection settings for a specified app. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ConnectionType** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPAppCmdlets.SetupAppAutoProvisionCmdlet+ConnectionTypes  <br/> |Specifies the connection type to provision.  <br/> |
|**EndPoint** <br/> |Required  <br/> |System.String  <br/> |Specifies the end point of the provision connection.  <br/> |
|**Password** <br/> |Required  <br/> |System.String  <br/> |Specifies the password for the provision connection.  <br/> |
|**Remove** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Removes the auto provision connection of the app.  <br/> |
|**Username** <br/> |Required  <br/> |System.String  <br/> |Specifies the user name of the connection.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the site collection for which the provision connection is to be associated.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ConnectionType** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPAppCmdlets.SetupAppAutoProvisionCmdlet+ConnectionTypes  <br/> ||
|**EndPoint** <br/> |Required  <br/> |System.String  <br/> ||
|**Password** <br/> |Required  <br/> |System.String  <br/> ||
|**Remove** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Username** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
   
## Example

------------EXAMPLE 1--------
  
```
Set-SpAppAutoProvisionConnection -ConnectionType RemoteWebHost -EndPoint https://SPremotewebhost -Password passname -Username <username>
```

This example configures remote web host to be used provision apps that use this functionality for the default site subscription server on http://SPremotewebhost.
  
------------EXAMPLE 2--------
  
```
$subscription = Get-SPSiteSubscription http://Contoso.com
```

```
Set-SPAppAutoProvisionConnection -ConnectionType RemoteWebHost -EndPoint https://SPremotewebhost -Password passname -Username <username> -SiteSubscription $subscription
```

This example configures remote web host to be used provision apps that use this functionality for the site subscription of Contoso.com site to server on http://SPremotewebhost. 
  
------------EXAMPLE 3--------
  
```
Set-SPAppAutoProvisionConnection -ConnectionType RemoteWebHost -EndPoint https://SPremotewebhost
```

This example updates the endpoint of the already configured remote web host server https://SPRemotewebhost for the default site subscription.
  
------------EXAMPLE 4--------
  
```
Set-SPAppAutoProvisionConnection -ConnectionType RemoteWebHost -Remove
```

This example removes the remote web host configuration for the default site subscription.
  
## See also

#### 

[Get-SPAppAutoProvisionConnection](get-spappautoprovisionconnection.md)

