---
title: "Remove-SPSiteSubscriptionFeaturePack"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 63a7bca5-17a1-4d3c-b2ff-9b35a456d6cb

description: "Removes a SharePoint Feature set from a site subscription."
---

# Remove-SPSiteSubscriptionFeaturePack

Removes a SharePoint Feature set from a site subscription.
  
```
Remove-SPSiteSubscriptionFeaturePack [-Identity] <SPSiteSubscriptionFeaturePackPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove- SPSiteSubscriptionFeaturePack** cmdlet removes a SharePoint Feature set by specifying the GUID or Feature set object. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPFeatureSetPipeBind  <br/> |Specifies the Feature set object to delete.  <br/>  The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of a feature set (for example, FeatureSet1); or an instance of a valid **SPFeatureSet** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionFeaturePackPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------------EXAMPLE------------------------
  
```
Remove-SPFeatureSet -Identity "30daa535-b0fe-4d10-84b0-fb04029d161a"
```

This example removes a SharePoint Feature set that has the ID  `30daa535-b0fe-4d10-84b0-fb04029d161a`.
  
## See also

#### 

[Get-SPSiteSubscriptionFeaturePack](get-spsitesubscriptionfeaturepack.md)
  
[New-SPSiteSubscriptionFeaturePack](new-spsitesubscriptionfeaturepack.md)
  
[Remove-SPSiteSubscriptionFeaturePack](remove-spsitesubscriptionfeaturepack.md)
  
[Add-SPSiteSubscriptionFeaturePackMember](add-spsitesubscriptionfeaturepackmember.md)

