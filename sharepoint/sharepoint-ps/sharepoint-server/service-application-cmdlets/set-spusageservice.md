---
title: "Set-SPUsageService"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 6/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c758e682-3a57-4d47-a932-56a96b56614d
description: "Updates the properties of a usage service."
---

# Set-SPUsageService

Updates the properties of a usage service.
  
```
Set-SPUsageService [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Identity <SPUsageServicePipeBind>] [-LoggingEnabled <$true | $false>] [-UsageLogCutTime <UInt32>] [-UsageLogLocation <String>] [-UsageLogMaxFileSizeKB <UInt32>] [-UsageLogMaxSpaceGB <UInt32>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------------------EXAMPLE-----------------
  
```
Set-SPUsageService -LoggingEnabled $false
```

```
Set-SPUsageService -UsageLogLocation "D:\\testusagelogdir"
```

```
Set-SPUsageService -UsageLogCutTime 5
```

The examples disables usage logging, changes the directory where usage files are stored, and creates a new usage log file every 5 minutes.
  
## Detailed Description

The **Set-SPUsageService** cmdlet updates the properties of a usage service. If the **Identity** parameter is not specified, the cmdlet applies the changes to the local usage service. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Identity_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUsageServicePipeBind  <br/> |Specifies the usage service to update.  <br/> The type must be in one of the following forms:  <br/> --A valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh  <br/> --A valid name of a usage service (for example, UsageService1)  <br/> --An instance of a valid **SPUsageService** object.  <br/> |
| _LoggingEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that usage data is logged to usage files.  <br/> |
| _UsageLogCutTime_ <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the time, in minutes, of usage data that is collected per usage log file. The default time is 5 minutes.  <br/> The value must be an integer in the range of 1 to 1440.  <br/> |
| _UsageLogLocation_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the path on every computer in the farm where usage log files are created.  <br/> The value must be a valid local path in the following form:  <br/> - C:\folder_name  <br/> |
| _UsageLogMaxFileSizeKB_ <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the maximum size of a single usage file that is applied to all the usage providers.  <br/> The minimum value is 512 kilobytes (KB) and the maximum value is 65536 KB.  <br/> |
| _UsageLogMaxSpaceGB_ <br/> |Optional  <br/> |System.UInt32  <br/> |The parameter is not used in SharePoint Server 2016.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUsageServicePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**LoggingEnabled** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**UsageLogCutTime** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**UsageLogLocation** <br/> |Optional  <br/> |System.String  <br/> ||
|**UsageLogMaxFileSizeKB** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**UsageLogMaxSpaceGB** <br/> |Optional  <br/> |System.UInt32  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPUsageService](get-spusageservice.md)

