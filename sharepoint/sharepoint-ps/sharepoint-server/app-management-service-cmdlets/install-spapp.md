---
title: "Install-SPApp"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2108d6a7-c17a-4c3a-86bb-1bfc282d60c1

description: "Installs an instance of an app."
---

# Install-SPApp

Installs an instance of an app.
  
```
Install-SPApp -Identity <SPApp> -Web <SPWebPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Install-SPApp** cmdlet to install an instance of an app within a web application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPApp  <br/> |Specifies the app to install. The App object is created by using the [Import-SPAppPackage](import-spapppackage.md) cmdlet.  <br/> |
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the web, either as an ID or URL, in which the app will be installed.  <br/> |
|**Web** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the **SPWeb** object of the app.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPApp  <br/> ||
|**Web** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------EXAMPLE------------
  
```
$spapp = Import-SPAppPackage -Path .\feature-upgrade-v1.spapp -Site http://localhost -Source ([microsoft.sharepoint.administration.spappsource]::ObjectModel)
```

```
$instance = Install-SPApp -Web http://localhost -Identity $spapp
```

This example installs an app by first importing the app package, and then installing it.
  
## See also

#### 

[Import-SPAppPackage](import-spapppackage.md)

