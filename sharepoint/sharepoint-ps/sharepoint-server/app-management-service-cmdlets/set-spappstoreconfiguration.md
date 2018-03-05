---
title: "Set-SPAppStoreConfiguration"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/1/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 72aa66c2-1d25-4a3c-bb84-45c443d26df1

description: "Sets SharePoint Store settings for an app."
---

# Set-SPAppStoreConfiguration

Sets SharePoint Store settings for an app.
  
```
Set-SPAppStoreConfiguration -Enable <$true | $false> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Url <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Set-SPAppStoreConfiguration** cmdlet to set SharePoint Store settings for a specified app. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Enable** <br/> |Required  <br/> |System.Boolean  <br/> |Specifies whether the Office Store services lets third- party add-ins to be found or downloaded.  <br/> This is intended for administrators to disable discovery and downloads of third-party add-ins on their SharePoint tenants and site collections.  <br/> The valid values are **True** and **False**.  <br/> The default value is **False**.  <br/> |
|**Url** <br/> |Optional  <br/> |System.String  <br/> |Specifies the URL of the app for which to set SharePoint Store settings.  <br/> > [!NOTE]> The SharePoint store value should not be changed unless instructed by a Microsoft representative.           |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Enable** <br/> |Required  <br/> |System.Boolean  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Url** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------EXAMPLE 1--------
  
```
Set-SPAppStoreConfiguration -Url http://office.microsoft.com -Enable $true
```

This example sets the URL to the Office.com server.
  
-----------EXAMPLE 2--------
  
```
Set-SPAppStoreConfiguration -Enable $false
```

This example turns off the SharePoint Store.
  
-----------EXAMPLE 3--------
  
```
Set-SPAppStoreConfiguration -Enable $true
```

This example turns on the SharePoint Store.
  
## See also

#### 

[Get-SPAppStoreConfiguration](get-spappstoreconfiguration.md)

