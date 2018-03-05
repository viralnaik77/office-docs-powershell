---
title: "Get-SPInsightsConfig"
ms.author: kirks
author: Techwriter40
ms.date: 9/7/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f5ac92b-d831-4d98-bf48-6601be53e007

description: "Returns the uploader.xml and Microsoft.Office.BigData.DataLoader.exe.config files from the Configuration database."
---

# Get-SPInsightsConfig

Returns the uploader.xml and Microsoft.Office.BigData.DataLoader.exe.config files from the Configuration database.
  
```
Get-SPInsightsConfig [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

--------------EXAMPLE 1-----------------
  
```
$config = Get-SPInsightsConfig
```

```
$xml = $config.UploaderXml
```

```
# Now we can do some modification to xml
$config.UploaderXml = $xml
$config.Update()
```

```
# Restart "Microsoft SharePoint Insights" service to provision this change to all farm servers 
Stop-SPService -Identity "Microsoft SharePoint Insights" 
Start-SPService -Identity "Microsoft SharePoint Insights" 

```

This example returns and modifies the config.uploader.xml file.
  
--------------EXAMPLE 2-----------------
  
```
$config = Get-SPInsightsConfig
```

```
$odlExeConfig = $config.OdlExeConfig
```

```
# Now we can do some modification to OdlExeConfig 
$config.OdlExeConfig = $odlExeConfig 
$config.Update()
```

```
# Restart "Microsoft SharePoint Insights" service to provision this change to all farm servers 
Stop-SPService -Identity "Microsoft SharePoint Insights" 
Start-SPService -Identity "Microsoft SharePoint Insights" 

```

This example returns and modifies the config.uploader.xml file.
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   

