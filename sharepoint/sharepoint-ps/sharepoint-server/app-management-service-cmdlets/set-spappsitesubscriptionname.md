---
title: "Set-SPAppSiteSubscriptionName"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13faea32-d626-4723-911e-8211069ade3d

description: "Sets or changes the name for the specified site subscription."
---

# Set-SPAppSiteSubscriptionName

Sets or changes the name for the specified site subscription.
  
```
Set-SPAppSiteSubscriptionName -Name <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-SiteSubscription <SPSiteSubscriptionPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Set-SPAppSiteSubscriptionName** cmdlet to set or change the name for a specified site subscription by using the **Name** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name for the site subscription.  <br/> Each site subscription must have a unique name. The name is used in part to determine the domain that apps for SharePoint are installed in for each site subscription.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |The site subscription name is recorded in other databases in the SharePoint farm. In cases such as disaster recovery or restore of the SharePoint farm, the **Force** parameter can be specified to ensure that the site subscription name has been propagated appropriately throughout the SharePoint farm.  <br/> |
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the **SPSiteSubscription** object or the **SPSiteSubscription Id** or the URL of an **SPSite**. If this parameter is not specified, then the default site subscription is used. All SharePoint **SPSites** are members of the default site subscription if they have not been specifically assigned a site subscription.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------EXAMPLE 1---------- 
  
```
Set-SPAppSiteSubscriptionName -Name Contoso
```

This example sets the name of the default site subscription to "Contoso".
  
-----------EXAMPLE 2---------- 
  
```
Set-SPAppSiteSubscriptionName -Name Contoso -SiteSubscription https://www.contoso.com
```

This example changes the name of the site subscription for **SPSite** from https://www.contoso.com to "Contoso". 
  
## See also

#### 

[Get-SPAppSiteSubscriptionName](get-spappsitesubscriptionname.md)

