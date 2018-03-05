---
title: "Get-SPSiteSubscriptionFeaturePack"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5b313a6b-fa12-45d7-9843-b4b17bf0bb8f

description: "Retrieves available SharePoint Feature sets or the Feature set assigned to a given site subscription."
---

# Get-SPSiteSubscriptionFeaturePack

Retrieves available SharePoint Feature sets or the Feature set assigned to a given site subscription.
  
```
Get-SPSiteSubscriptionFeaturePack [[-Identity] <SPSiteSubscriptionFeaturePackPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Get-SPSiteSubscriptionFeaturePack** cmdlet retrieves available SharePoint Feature sets or the Feature set assigned to a given site subscription. 
  
> [!CAUTION]
> Be careful when you assign Feature sets to variables because changes to the Feature set are not reflected until the variable is refreshed. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPFeatureSetPipeBind  <br/> |Specifies a valid name or GUID of the Feature set.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |If provided, ensures that the returned Feature set is the Feature set that is currently assigned to the given site subscription.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionFeaturePackPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
   
## Example

------------------EXAMPLE 1------------------
  
```
Get- SPSiteSubscriptionFeaturePack
```

This example returns all defined Feature sets in the local farm.
  
------------------EXAMPLE 2------------------
  
```
Get-SPSiteSubscriptionFeaturePack -SiteSubscription http://contoso.com | ForEach{ $_.FeatureDefinitions }
```

This example returns the list (name, ID, and scope) of all Features allowed in the Feature set that is currently assigned to the site subscription of  `http://contoso.com`.
  
## See also

#### 

[New-SPSiteSubscriptionFeaturePack](new-spsitesubscriptionfeaturepack.md)
  
[Remove-SPSiteSubscriptionFeaturePack](remove-spsitesubscriptionfeaturepack.md)
  
[Add-SPSiteSubscriptionFeaturePackMember](add-spsitesubscriptionfeaturepackmember.md)

