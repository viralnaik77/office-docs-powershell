---
title: "Install-SPDataConnectionFile"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a8878fd9-a8b4-44aa-9c48-0b688bd50a91

description: "Installs the provided data connection file."
---

# Install-SPDataConnectionFile

Installs the provided data connection file.
  
```
Install-SPDataConnectionFile [-Path] <String> [-AssignmentCollection <SPAssignmentCollection>] [-Category <String>] [-Confirm [<SwitchParameter>]] [-Overwrite <SwitchParameter>] [-WebAccessible <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Install-SPDataConnectionFile** cmdlet installs the provided data connection file. If the specified data connection file exists, the user is prompted to replace the existing file. 
  
This cmdlet does not create a new file. Instead, it creates a new data connection file object.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies the full path to the name of the file in the data connection store.  <br/> The type must be the name of a valid data connection file; for example, C:\foldername\myconnection.udcx.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Category** <br/> |Optional  <br/> |System.String  <br/> |Sets an arbitrary category on the file which can be used to group the files. The category name can have a maximum of 255 characters.  <br/> The type must be a valid string value; for example, Category1.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Overwrite** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Overwrites the existing data connection file. The default value is **False**.  <br/> |
|**WebAccessible** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the universal data connection file can be accessed by using the Web service. If **False**, only the Forms Server 2013 can retrieve the universal data connection files internally. The default value is **False**.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Category** <br/> |Optional  <br/> |System.String  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Overwrite** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WebAccessible** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------EXAMPLE--------------
  
```
Install-SPDataConnectionFile -Path .\folder\sample.udcx -Category "Install" -WebAccessible $true
```

```
".\folder\sample.udcx" | Install-SPDataConnectionFile -Category "Install" -Category "Category1"  -Overwrite $true
```

This example uploads a data connection file to a specified category.
  
This cmdlet is equivalent to the **Upload Data Connection File** user interface setting that is located on the Manage Data Connection Files page of the SharePoint Central Administration Web site. 
  
## See also

#### 

[Get-SPDataConnectionFile](get-spdataconnectionfile.md)
  
[Set-SPDataConnectionFile](set-spdataconnectionfile.md)
  
[Uninstall-SPDataConnectionFile](uninstall-spdataconnectionfile.md)

