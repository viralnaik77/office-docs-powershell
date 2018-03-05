---
title: "Remove-SPServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd1eb4ce-632a-46fb-8a0a-0cfd28172e7b

description: "Deletes the specified service application on the local server."
---

# Remove-SPServiceApplication

Deletes the specified service application on the local server.
  
```
Remove-SPServiceApplication [-Identity] <SPServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-RemoveData <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPServiceApplication** cmdlet deletes the specified service application from the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> |Specifies the GUID of the service application to remove.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**RemoveData** <br/> |Optional  <br/> |SwitchParameter  <br/> |Deletes all databases and other data associated with the service application.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**RemoveData** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------------EXAMPLE---------------------------
  
```
Remove-SPServiceApplication 053c34be-d251-488c-8e94-644eae94da26 -RemoveData
```

This example deletes the service application and its database.
  
The service application GUID is unique to every farm. You can run the **Get-SPServiceApplication** cmdlet to see the GUID of the service applications, and then use the result from the **Get-SPServiceApplication** cmdlet for other **SPServiceApplication** cmdlets; for example, or **Publish-SPServiceApplication**. 
  
## See also

#### 

[Get-SPServiceApplication](get-spserviceapplication.md)
  
[Set-SPServiceApplication](set-spserviceapplication.md)
  
[Publish-SPServiceApplication](publish-spserviceapplication.md)

