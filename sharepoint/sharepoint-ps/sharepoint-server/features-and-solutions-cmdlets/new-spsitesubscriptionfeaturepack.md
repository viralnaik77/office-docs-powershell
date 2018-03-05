---
title: "New-SPSiteSubscriptionFeaturePack"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5d7a400-6d7c-4e0f-a0ef-e4d16f878208

description: "Creates a new SharePoint Feature set that can be used to limit the features available to a site subscription."
---

# New-SPSiteSubscriptionFeaturePack

Creates a new SharePoint Feature set that can be used to limit the features available to a site subscription.
  
```
New-SPSiteSubscriptionFeaturePack [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **New- SPSiteSubscriptionFeaturePack** cmdlet to create a new SharePoint Feature set that limits the Features available to a specified site subscription. 
  
SharePoint Feature sets are on an Allow List of SharePoint Features that can be associated with any site subscription. If a Feature set is assigned to a site subscription, only **SPFeatures** objects in that Feature set are available for use on the site collections and Webs that are members of the site subscription. Feature sets contain a list of the GUIDs of each Feature that is on an Allow List for associated site subscriptions. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
$fs = New-SPSiteSubscriptionFeaturePack
```

This example creates a new SharePoint Feature set and stores it in a variable.
  
## See also

#### 

[Get-SPSiteSubscriptionFeaturePack](get-spsitesubscriptionfeaturepack.md)
  
[Add-SPSiteSubscriptionFeaturePackMember](add-spsitesubscriptionfeaturepackmember.md)
  
[New-SPSiteSubscriptionFeaturePack](new-spsitesubscriptionfeaturepack.md)
  
[Add-SPSiteSubscriptionFeaturePackMember](add-spsitesubscriptionfeaturepackmember.md)

