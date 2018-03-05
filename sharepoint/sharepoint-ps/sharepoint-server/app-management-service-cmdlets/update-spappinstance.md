---
title: "Update-SPAppInstance"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67a1ec19-39f3-46fe-8712-25f0ec5d4a9c

description: "Updates the app instance."
---

# Update-SPAppInstance

Updates the app instance.
  
```
Update-SPAppInstance -App <SPApp> -Identity <SPAppInstance> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Update-SPAppInstance** cmdlet to update the app instance. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**App** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPApp  <br/> |Specifies the app version to upgrade to.  <br/> |
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPAppInstance  <br/> |Specifies The app instance to upgrade.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**App** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPApp  <br/> ||
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPAppInstance  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------EXAMPLE--------- 
  
```
$spapp = Import-SPAppPackage -Path .\feature-upgrade-v2.spapp -Site http://localhost -Source ([microsoft.sharepoint.administration.spappsource]::ObjectModel)
```

```
$instance = Get-SPAppInstance -AppInstanceId $instance.Id
```

```
Update-SPAppInstance -Identity $instance -App $spapp
```

This example updates an instance of an app.
  
## See also

#### 

[Get-SPAppInstance](get-spappinstance.md)
  
[Uninstall-SPAppInstance](uninstall-spappinstance.md)
#### 

[Restart-SPAppInstanceJobs](http://technet.microsoft.com/library/582e2939-1a82-47fc-b1f5-f405f37196f3.aspx)

