---
title: "New-SPTranslationServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d7d70790-7105-4c20-af54-c13f0fa3ec75

description: "Creates a Machine Translation Service application proxy on the local farm."
---

# New-SPTranslationServiceApplicationProxy

Creates a Machine Translation Service application proxy on the local farm.
  
```
New-SPTranslationServiceApplicationProxy -Name <String> -ServiceApplication <TranslationServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DefaultProxyGroup <SwitchParameter>] [-PartitionMode <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **New-SPTranslationServiceApplicationProxy** cmdlet creates a Machine Translation Service application proxy on the local farm. The proxy is added to the default proxy group for the local farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the display name for the new Machine Translation Service application. The name that you use must be a unique name of a Machine Translation Service application in this farm. The name can be a maximum of 128 characters.  <br/> |
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.Office.TranslationServices.Powershell.TranslationServiceApplicationPipeBind  <br/> |Specifies the local Machine Translation Service application that is associated with the new proxy.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a Machine Translation Service application (for example, MachTrans1); or an instance of a valid **SPServiceApplication** object.  <br/> |
|**Uri** <br/> |Required  <br/> |System.String  <br/> |Specifies the URI of the remote machine translation service application this proxy should communicate with. This value is required only if you plan to connect a Machine Translation Service application from a remote farm.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the Machine Translation Service application proxy be added to the default proxy group for the local farm.  <br/> |
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the service application restrict data by site group. After the **PartitionMode** parameter is set and the service application is created, it cannot be changed  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.Office.TranslationServices.Powershell.TranslationServiceApplicationPipeBind  <br/> ||
|**Uri** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------EXAMPLE---------
  
```
New-SPTranslationServiceApplicationProxy -Name TranslationServiceProxy -ServiceApplication TranslationService -DefaultProxyGroup
```

This example creates a Machine Translation Service application proxy in the default proxy group named TranslationServiceProxy which connects to the Machine Translation Service application named TranslationService.
  
## See also

#### 

[New-SPTranslationServiceApplication](new-sptranslationserviceapplication.md)
  
[Set-SPTranslationServiceApplication](set-sptranslationserviceapplication.md)
  
[Set-SPTranslationServiceApplicationProxy](set-sptranslationserviceapplicationproxy.md)

