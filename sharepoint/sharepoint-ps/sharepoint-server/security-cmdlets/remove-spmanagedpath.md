---
title: "Remove-SPManagedPath"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6b6daf4a-4102-4583-9da7-9f0433d87b19

description: "Deletes the specified managed path from the specified host header or Web application."
---

# Remove-SPManagedPath

Deletes the specified managed path from the specified host header or Web application.
  
```
Remove-SPManagedPath [-Identity] <SPPrefixPipeBind> -WebApplication <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Remove-SPManagedPath** cmdlet deletes the managed path specified by the **Identity** parameter from the host header or the Web application. The **Identity** must be the partial URL of the managed path to be deleted. 
  
If you are using host headers, specify the **HostHeader** parameter. To delete a HostHeader managed path, provide the **HostHeader** switch. Otherwise, you must specify the Web application that contains the managed path to be deleted. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPPrefixPipeBind  <br/> |Specifies the name of the managed path to delete. For example, in the URL http://sitename/sites/site1, "sites" is the name of the managed path.  <br/> |
|**HostHeader** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the **Identity** is a host header managed path.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.WebApplicationPipeBind  <br/> |Specifies the identity of the Web application that hosts the managed path to delete. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid Web application name (for example, WebApplication1212); or a valid name, in the form WebApp2423.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPPrefixPipeBind  <br/> ||
|**HostHeader** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

----------------------EXAMPLE 1----------------------------
  
```
Remove-SPManagedPath "sites" -HostHeader
```

This example removes the  `sites` managed path from the list of  `HostHeader` managed paths. 
  
Depending on the confirmation level of the local system, the preceding example can prompt prior to execution.
  
------------------EXAMPLE 2-----------------------
  
```
Get-SPWebApplication | Remove-SPManagedPath "personal" -confirm:$false
```

This example removes the  `personal` managed path from all Web applications in the farm. This command does not prompt for confirmation. 
  
## See also

#### 

[Get-SPManagedPath](get-spmanagedpath.md)
  
[New-SPManagedPath](new-spmanagedpath.md)

