---
title: "Set-SPTranslationServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1f83fcc6-7a71-4343-8bde-21856283ec3f

description: "Sets properties to the Machine Translation service application proxy."
---

# Set-SPTranslationServiceApplicationProxy

Sets properties to the Machine Translation service application proxy.
  
```
Set-SPTranslationServiceApplicationProxy -Identity <TranslationServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DefaultProxyGroup <SwitchParameter>] [-MaximumGroupSize <Int32>] [-MaximumItemCount <Int32>] [-WhatIf [<SwitchParameter>]]

```

## Example

-------------EXAMPLE---------
  
```
Set-SPTranslationServiceApplicationProxy TranslationServiceProxy -DefaultProxyGroup
```

This example adds the Machine Translation Service application proxy named TranslationServiceProxy to the default proxy group.
  
## Detailed Description

Use the **Set-SPTranslationServiceApplicationProxy** cmdlet to set properties on a Machine Translation service application proxy in the farm. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.TranslationServices.Powershell.TranslationServiceApplicationProxyPipeBind  <br/> |Specifies the GUID of the service application proxy.  <br/> The type must be a valid GUID in the form, 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DefaultProxyGroup_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the Machine Translation Service application proxy be added to the default proxy group for the local farm.  <br/> |
| _MaximumGroupSize_ <br/> |Optional  <br/> |System.Int32  <br/> |Maximum number of bytes the proxy will send to the service in a single request. The valid values are 131072 to 10485760. The default value is 2097152.  <br/> > [!NOTE]> We do not recommend use of this parameter.           |
| _MaximumItemCount_ <br/> |Optional  <br/> |System.Int32  <br/> |Maximum number of documents to be translated that the proxy will send to the service in a single request. The valid values are 1 to 40960. The default value is 9000.  <br/> > [!NOTE]> We do not recommend use of this parameter.           |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.TranslationServices.Powershell.TranslationServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**MaximumGroupSize** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaximumItemCount** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPTranslationServiceApplication](new-sptranslationserviceapplication.md)
  
[New-SPTranslationServiceApplicationProxy](new-sptranslationserviceapplicationproxy.md)
  
[Set-SPTranslationServiceApplication](set-sptranslationserviceapplication.md)

