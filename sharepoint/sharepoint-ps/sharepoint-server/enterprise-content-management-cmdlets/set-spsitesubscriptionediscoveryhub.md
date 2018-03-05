---
title: "Set-SPSiteSubscriptionEdiscoveryHub"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c21e9b02-9208-4dc8-87e5-17055db44e9e

description: "Sets properties for the eDiscovery hub of a site subscription."
---

# Set-SPSiteSubscriptionEdiscoveryHub

Sets properties for the eDiscovery hub of a site subscription.
  
```
Set-SPSiteSubscriptionEdiscoveryHub -Site <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-SearchScope <String>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------------------EXAMPLE-------------------- 
  
```
Set-SPSiteSubscriptionEdiscoverySearchScope -Site http://contoso.com/sites/sitecollection1 -SearchScope 1

```

This example enables the search scope for the entire site subscription. A value of zero (0) disables the search scope across the entire site subscription.
  
## Detailed Description

The **Set-SPSiteSubscriptionEdiscoveryHub** cmdlet sets global properties and settings for the Ediscovery hub. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Site_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the site collection for the Ediscovery hub.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _SearchScope_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name for the search scope. The default value is **All Sites**.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SearchScope** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPSiteSubscriptionEdiscoveryHub](get-spsitesubscriptionediscoveryhub.md)
  
[Get-SPSiteSubscriptionEdiscoverySearchScope](get-spsitesubscriptionediscoverysearchscope.md)

