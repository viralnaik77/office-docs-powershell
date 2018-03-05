---
title: "Set-SPUsageDefinition"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/8/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 05ff2fea-1955-4537-8cfb-1b0e3890e1be

description: "Sets the retention period for a usage provider."
---

# Set-SPUsageDefinition

Sets the retention period for a usage provider.
  
```
Set-SPUsageDefinition -Identity <SPUsageDefinitionPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DaysRetained <Int32>] [-DaysToKeepUsageFiles <Int32>] [-Enable <SwitchParameter>] [-MaxTotalSizeInBytes <Int64>] [-UsageDatabaseEnabled <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

-----------------EXAMPLE--------------------
  
```
Set-SPUsageDefinition -Identity "Page Requests" -DaysRetained 31
```

This example sets the number of days that stores page requests usage data to 31.
  
## Detailed Description

The **Set-SPUsageDefinition** cmdlet sets the retention period for a specified usage provider. A usage definition object defines a specific type of usage provider. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUsageDefinitionPipeBind  <br/> |Specifies the usage definition object to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a usage definition (for example, SiteSubscriptionConfig1); or an instance of a valid **SPUsageDefinition** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DaysRetained_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of days that usage data for the usage provider is retained in the usage service database. The default value is **14**.  <br/> The type must be an integer between 0 and 31.  <br/> |
| _DaysToKeepUsageFiles_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of days to keep usage file retention. The value must be less than or equal to value of the **DaysRetained** parameter.  <br/> |
| _Enable_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Turns on the specified usage provider.  <br/> |
| _MaxTotalSizeInBytes_ <br/> |Optional  <br/> |System.Int64  <br/> |Specifies the max size of retention in bytes.  <br/> |
| _UsageDatabaseEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether usage database should be enabled.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUsageDefinitionPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DaysRetained** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**DaysToKeepUsageFiles** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**Enable** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**MaxTotalSizeInBytes** <br/> |Optional  <br/> |System.Int64  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPUsageDefinition](get-spusagedefinition.md)

