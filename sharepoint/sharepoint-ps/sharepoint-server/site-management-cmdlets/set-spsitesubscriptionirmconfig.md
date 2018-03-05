---
title: "Set-SPSiteSubscriptionIRMConfig"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e46871e5-b806-48c6-9cc5-eb901b21b2d2

description: "Sets the Information Rights Management (IRM) settings."
---

# Set-SPSiteSubscriptionIRMConfig

Sets the Information Rights Management (IRM) settings.
  
```
Set-SPSiteSubscriptionIRMConfig [-Identity] <SPSiteSubscriptionPipeBind> -IrmEnabled <SwitchParameter> [-AssignmentCollection <SPAssignmentCollection>] [-CertificateServerUrl <Uri>] [-Confirm [<SwitchParameter>]] [-PassThru <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Identity** parameter of the **Set-SPSiteSubscriptionIRMConfig** cmdlet to set the IRM setting for a specified tenant. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies a site subscription for a particular tenant.  <br/> |
|**IrmEnabled** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether IRM is enabled in the tenant.  <br/> The default value is false.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CertificateServerUrl** <br/> |Optional  <br/> |System.Uri  <br/> |Specifies the address of the RMS certificate server to use for the tenant.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**PassThru** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the output object can be passed through the pipeline.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**IrmEnabled** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CertificateServerUrl** <br/> |Optional  <br/> |System.Uri  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**PassThru** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------EXAMPLE 1------------ 
  
```
site = Get-SPSite  HYPERLINK "http://<myspserver>" http:// <myspserver>
```

```
$subscription = $site.SiteSubscription
```

```
Set-SPSiteSubscriptionIRMConfig -Identity $subscription -IrmEnabled -CertificateServerUrl http:// <rmsserver>
```

This example enables IRM for the tenant and configures it to use the specified RMS server.
  
--------------EXAMPLE 2------------ 
  
```
site = Get-SPSite  HYPERLINK "http://myspserver" http:// <myspserver>
```

```
$subscription = $site.SiteSubscription
```

```
Set- SPSiteSubscriptionIRMConfig -Identity $subscription -IrmEnabled:$false
```

This example disables IRM for the tenant.
  
## See also

#### 

[Get-SPSiteSubscriptionIRMConfig](get-spsitesubscriptionirmconfig.md)

