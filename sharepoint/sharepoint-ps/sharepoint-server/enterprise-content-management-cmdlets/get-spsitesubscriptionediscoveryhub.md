---
title: "Get-SPSiteSubscriptionEdiscoveryHub"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1464ce1d-ba55-4c2a-b5a1-6854c37d1115

description: "Displays the eDiscovery hub for a site subscription."
---

# Get-SPSiteSubscriptionEdiscoveryHub

Displays the eDiscovery hub for a site subscription.
  
```
Get-SPSiteSubscriptionEdiscoveryHub -Identity <SPSiteSubscriptionPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE----------------------
  
```
Get-SPSiteSubscriptionEdiscoveryHub -Identity http://contoso.com

```

This example displays the eDiscovery hub for the specified site collection.
  
## Detailed Description

Use the **Get-SPSiteSubscriptionEdiscoveryHub** cmdlet to display the site collection configured as the eDiscovery hub for the specified site subscription. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the URL of the site collections to the eDiscovery hub. Can pipe the result from the **Get-SPSiteSubcription** cmdlet.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPSiteSubscriptionEdiscoverySearchScope](get-spsitesubscriptionediscoverysearchscope.md)
  
[Set-SPSiteSubscriptionEdiscoveryHub](set-spsitesubscriptionediscoveryhub.md)

