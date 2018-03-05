---
title: "Remove-SPSiteSubscriptionFeaturePackMember"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 041adee7-5d8f-4229-920c-7a95dd6dba89

description: "Removes a feature definition from the provided SharePoint Feature set."
---

# Remove-SPSiteSubscriptionFeaturePackMember

Removes a feature definition from the provided SharePoint Feature set.
  
```
Remove-SPSiteSubscriptionFeaturePackMember [-Identity] <SPSiteSubscriptionFeaturePackPipeBind> -FeatureDefinition <SPFeatureDefinitionPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Remove-SPSiteSubscriptionFeaturePackMember** cmdlet removes the provided **FeatureDefintion** parameter from the feature set specified by the **Identity** parameter. If the **AllFeatureDefinitions** flag is provided, all feature definitions are removed from the given Feature set. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPFeatureSetPipeBind  <br/> |Specifies the Feature set from which to remove a feature.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of a feature set (for example, FeatureSet1); or an instance of a valid **SPFeatureSet** object.  <br/> |
|**AllFeatureDefinitions** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Clears all features from the Feature set.  <br/> |
|**FeatureDefinition** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPFeatureDefinitionPipeBind  <br/> |Specifies the feature definition to be removed.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionFeaturePackPipeBind  <br/> ||
|**AllFeatureDefinitions** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**FeatureDefinition** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPFeatureDefinitionPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1-----------------------
  
```
$FS = Get-SPSiteSubscriptionFeaturePack "30daa535-b0fe-4d10-84b0-fb04029d161a"
```

```
Remove-SPSiteSubscriptionFeaturePackMember -Identity $fs -FeatureDefinition (Get-SPFeature "PublishingSite")
```

This example removes the  `PublishingSite` feature from the Feature set that has ID  `30daa535-b0fe-4d10-84b0-fb04029d161a`.
  
------------------EXAMPLE 2-----------------------
  
```
Get-SPSiteSubscriptionFeaturePack "30daa535-b0fe-4d10-84b0-fb04029d161a" | Remove-SPSiteSubscriptionFeaturePackMember -AllFeatureDefinitions
```

This example removes all features from the Feature set  `30daa535-b0fe-4d10-84b0-fb04029d161a`.
  
## See also

#### 

[Add-SPSiteSubscriptionFeaturePackMember](add-spsitesubscriptionfeaturepackmember.md)
  
[Get-SPSiteSubscriptionFeaturePack](get-spsitesubscriptionfeaturepack.md)
  
[Remove-SPSiteSubscriptionFeaturePack](remove-spsitesubscriptionfeaturepack.md)

