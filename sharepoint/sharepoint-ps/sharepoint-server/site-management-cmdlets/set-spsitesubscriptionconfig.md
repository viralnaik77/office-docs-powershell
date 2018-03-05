---
title: "Set-SPSiteSubscriptionConfig"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3a4edbaf-d84a-4afa-8b4b-c725b06c1a74

description: "Sets the configuration properties of a site subscription."
---

# Set-SPSiteSubscriptionConfig

Sets the configuration properties of a site subscription.
  
```
Set-SPSiteSubscriptionConfig [-Identity] <SPSiteSubscriptionPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-FeaturePack <SPSiteSubscriptionFeaturePackPipeBind>] [-PassThru <SwitchParameter>] [-UserAccountDirectoryPath <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPSiteSubscriptionConfig** cmdlet sets the configuration properties of a site subscription. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the site subscription configuration to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; an SPSite (object or URL) of a site collection that is a member of the site subscription; or an instance of a valid **SiteSubscription** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**PassThru** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies the output object can be passed through the pipeline.  <br/> |
|**FeatureSet** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPFeatureSetPipeBind  <br/> |Specifies the feature set that is associated with the site subscription.  <br/> Specifies a null value to clear the current association.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid **SPFeatureSet**object.  <br/> |
|**UserAccountDirectoryPath** <br/> |Optional  <br/> |System.String  <br/> |Sets the site user account directory path to a specific organizational unit (OU) that is in the same domain as the site subscription.  <br/> The type must be a name of a distinguished OU; for example, OU=Contoso1, DC=OSGCorp,DC=local.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**FeaturePack** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionFeaturePackPipeBind  <br/> ||
|**PassThru** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**UserAccountDirectoryPath** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------EXAMPLE---------------
  
```
Set-SPSiteSubscription http://contoso.com -FeatureSet 12345678-90ab-cdef-1234-567890abcdef
```

This example sets the Feature set of the entire site subscription that contains  `http://contoso.com` with a Feature set GUID. 
  

