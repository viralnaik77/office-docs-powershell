---
title: "Remove-SPServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf337d34-54b0-4919-9c48-2ad4d50b8328

description: "Deletes the specified service application proxy."
---

# Remove-SPServiceApplicationProxy

Deletes the specified service application proxy.
  
```
Remove-SPServiceApplicationProxy [-Identity] <SPServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-RemoveData <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPServiceApplicationProxy** cmdlet deletes the service application proxy specified by the **Identity** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the GUID of the service application proxy to remove.  <br/> The type must be a GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
|**RemoveData** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Deletes all databases and other data associated with the service application proxy.  <br/> |
|**AssignmentColletion** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentColletion  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**RemoveData** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
Remove-SPServiceApplicationProxy babab30e-8e3a-428b-8ff4-4d5c8f455e6d
```

This example deletes the given service application proxy.
  
The service application GUID is unique to every farm. You can run the **Get-SPServiceApplication** cmdlet to see the GUID of the service applications, and then use the result from the **Get-SPServiceApplication** cmdlet for other **SPServiceApplication** cmdlets; for example, **Grant-SPServiceApplication** or **Publish-SPServiceApplication**. 
  
## See also

#### 

[Get-SPServiceApplicationProxy](get-spserviceapplicationproxy.md)
  
[New-SPServiceApplicationProxyGroup](new-spserviceapplicationproxygroup.md)
  
[Remove-SPServiceApplicationProxy](remove-spserviceapplicationproxy.md)

