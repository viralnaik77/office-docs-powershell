---
title: "Add-SPSiteSubscriptionFeaturePackMember"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d97423ee-5bdb-4c54-8408-7044aac7d789

description: "Adds a feature to a SharePoint Feature set."
---

# Add-SPSiteSubscriptionFeaturePackMember

Adds a feature to a SharePoint Feature set.
  
```
Add-SPSiteSubscriptionFeaturePackMember [-Identity] <SPSiteSubscriptionFeaturePackPipeBind> -FeatureDefinition <SPFeatureDefinitionPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Add- SPSiteSubscriptionFeaturePackMember** cmdlet adds features to the provided SharePoint Feature set. Feature sets are an Allow List of SharePoint Features that can be associated with any site subscription. If a Feature set is assigned to a site subscription, only the **SPFeatures** object in that Feature set are available for use on the site collections and Web sites that are members of the site subscription. Feature sets contain a list of the GUIDs of each Feature that are on the Allow List for associated site subscriptions. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPFeatureSetPipeBind  <br/> |Specifies the Feature set object or GUID to which the given SharePoint Feature is added.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid name of a Feature set (for example, FeatureSet1); or an instance of a valid **SPFeatureSet** object.  <br/> |
|**FeatureDefinition** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPFeatureDefinitionPipeBind  <br/> |Specifies the Feature definition, name, or GUID to add to the Feature set.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionFeaturePackPipeBind  <br/> ||
|**FeatureDefinition** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPFeatureDefinitionPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-------------EXAMPLE----------------
  
```
$fs = New-SPFeatureSet
```

```
Get-SPFeature -limit all | Where{ $_.Scope -eq "WEB" } | Add-SPSiteSubscriptionFeaturePackMember -id $fs
```

```
$fs = Get-SPFeatureSet $fs
```

This example creates a Feature set and adds all Web site scoped Features to the set.
  
The Feature set is refreshed in the last line so that the local object has the correct values.
  
## See also

#### 

[Remove-SPSiteSubscriptionFeaturePackMember](remove-spsitesubscriptionfeaturepackmember.md)

