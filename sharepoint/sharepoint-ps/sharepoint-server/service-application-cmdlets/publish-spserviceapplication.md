---
title: "Publish-SPServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ddfa710-05cd-4d1c-83b7-8528f6ed12ad

description: "Shares the specified local service application outside the farm."
---

# Publish-SPServiceApplication

Shares the specified local service application outside the farm.
  
```
Publish-SPServiceApplication [-Identity] <SPServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Description <String>] [-InfoLink <Uri>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Publish-SPServiceApplication** cmdlet publishes the local service application, specified by the **Identity** parameter, outside the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> |Specifies the GUID of the service application to share outside the farm.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Description** <br/> |Optional  <br/> |System.String  <br/> |Describes the service application to share outside the farm. If no value is specified, the value is left blank.  <br/> |
|**InfoLink** <br/> |Optional  <br/> |System.Uri  <br/> |Specifies the link to more information about the service application to share outside the farm. If no link is specified, no link is made available.  <br/> The type must be a valid URL, in the form http://server_name/Site_Name/page_name.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Description** <br/> |Optional  <br/> |System.String  <br/> ||
|**InfoLink** <br/> |Optional  <br/> |System.Uri  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
Publish-SPServiceApplication 053c34be-d251-488c-8e94-644eae94da26 -Description "Connect to this TestServiceApplcation of you want to use FeatureA in your farm" -InfoLink http://testurl 
```

This example publishes a service application to another farm.
  
The service application GUID is unique to every farm. You can run the **Get-SPServiceApplication** cmdlet to see the GUID of the service applications, and then use the result from the **Get-SPServiceApplication** cmdlet for other **SPServiceApplication** cmdlets; for example, **Grant-SPServiceApplication**. 
  
## See also

#### 

[Get-SPServiceApplication](get-spserviceapplication.md)
  
[Set-SPServiceApplication](set-spserviceapplication.md)
  
[Remove-SPServiceApplication](remove-spserviceapplication.md)

