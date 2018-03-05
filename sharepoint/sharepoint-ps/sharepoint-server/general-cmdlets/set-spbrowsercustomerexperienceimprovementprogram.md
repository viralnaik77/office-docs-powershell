---
title: "Set-SPBrowserCustomerExperienceImprovementProgram"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/20/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22fad9d4-2e44-40c2-b42e-472c86999462

description: "Turns on or off the browser Customer Experience Improvement Program."
---

# Set-SPBrowserCustomerExperienceImprovementProgram

Turns on or off the browser Customer Experience Improvement Program.
  
```
Set-SPBrowserCustomerExperienceImprovementProgram -Farm <SwitchParameter> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Enable <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Set-SPBrowserCustomerExperienceImprovementProgram** cmdlet turns on or off the browser Customer Experience Improvement Program for collecting software quality metrics. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Farm** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Sets the farm to be included in the Customer Experience Improvement Program.  <br/> The default value is **True**.  <br/> |
|**SiteSubscription** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Sets the Customer Experience Improvement Program opt-in state for the specified site subscription.  <br/> The type must be a valid URL, in the form http://server_name; a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a site subscription (for example, SiteSubscription1); or an instance of a valid **SiteSubscription** object.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Sets the Customer Experience Improvement Program opt-in state for the specified SharePoint Web application.  <br/> The type must be a valid URL, in the form http://server_name; a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of SharePoint Web application (for example, MyOfficeApp1); or an instance of a valid **SPWebApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Enable** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Turns on the browser Customer Experience Improvement Program. The default value is **True**.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Farm** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SiteSubscription** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Enable** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1-----------------------
  
```
Set-SPBrowserCustomerExperienceImprovementProgram -Farm -Enable
```

This example turns on the browser Customer Experience Improvement Program for the farm.
  
------------------EXAMPLE 2-----------------------
  
```
Set-SPBrowserCustomerExperienceImprovementProgram -Farm -Enable:$False
```

This example turns off the browser Customer Experience Improvement Program for the farm.
  
------------------EXAMPLE 3-----------------------
  
```
Set-SPWebApplication http://MyOfficeApp1 | Get- SPBrowserCustomerExperienceImprovementProgram -Enable
```

This example turns on the browser Customer Experience Improvement Program for the Web application,  `MyOfficeApp1`.
  
## See also

#### 

[Get-SPBrowserCustomerExperienceImprovementProgram](get-spbrowsercustomerexperienceimprovementprogram.md)

