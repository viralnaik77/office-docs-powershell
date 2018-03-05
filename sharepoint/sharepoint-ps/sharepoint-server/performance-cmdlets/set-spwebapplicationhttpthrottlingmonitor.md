---
title: "Set-SPWebApplicationHttpThrottlingMonitor"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee7975ad-13d8-4365-bcab-6209fd803aa8

description: "Sets the Health Score bucket values for an existing network throttling performance counter for a specified Web application."
---

# Set-SPWebApplicationHttpThrottlingMonitor

Sets the Health Score bucket values for an existing network throttling performance counter for a specified Web application.
  
```
Set-SPWebApplicationHttpThrottlingMonitor [-Identity] <SPWebApplicationPipeBind> [-Category] <String> [-Counter] <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-HealthScoreBuckets <Double[]>] [-Instance <String>] [-IsDESC <SwitchParameter>] [-LowerLimit <Double>] [-UpperLimit <Double>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPWebApplicationHttpThrottlingMonitor** cmdlet sets the Health Score bucket values for an existing network throttling performance counter for a specified Web application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the SharePoint Web application to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint Web application (for example, MyOfficeApp1); or an instance of a valid **SPWebApplication** object.  <br/> |
|**Category** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the performance counter category.  <br/> The type must be a valid performance counter category in the throttling monitor. Use the **Get-SPWebApplicationHttpThrottlingMonitor** cmdlet to return a list of performance counter categories in the throttling monitor.  <br/> |
|**Counter** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the performance counter.  <br/> The type must be a valid performance counter in the throttling monitor. Use the **Get-SPWebApplicationHttpThrottlingMonitor** cmdlet to return a list of performance counters in the throttling monitor.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**HealthScoreBuckets** <br/> |Optional  <br/> |System.Double[]  <br/> |Specifies bucket ranges to use in determining the calculation of the server Health Score for this counter.  <br/> |
|**Instance** <br/> |Optional  <br/> |System.String  <br/> |Specifies the instance of the performance counter. The default value is empty. If the specified value is invalid, this cmdlet will not run.  <br/> |
|**IsDESC** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that this counter is interpreted in descending order.  <br/> If this parameter is set, Health Score bucket values are interpreted in descending order; for example, set this parameter by using the **Memory** category and **Available Mbytes** counter to monitor available memory.  <br/> |
|**LowerLimit** <br/> |Optional  <br/> |System.Double  <br/> |Specifies the lower limit of the numerical threshold of the specified performance counter. The lower limit is the lowest value in the Health Score bucket values.  <br/> |
|**UpperLimit** <br/> |Optional  <br/> |System.Double  <br/> |Specifies the upper limit of the numerical threshold of the specified performance counter. The upper limit is the highest value in the Health Score bucket values.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**Category** <br/> |Required  <br/> |System.String  <br/> ||
|**Counter** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**HealthScoreBuckets** <br/> |Optional  <br/> |System.Double[]  <br/> ||
|**Instance** <br/> |Optional  <br/> |System.String  <br/> ||
|**IsDESC** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**LowerLimit** <br/> |Optional  <br/> |System.Double  <br/> ||
|**UpperLimit** <br/> |Optional  <br/> |System.Double  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1------------------
  
```
$buckets=(2000,1000,500,300,200,100,50,30,20,10)Set-SPWebApplicationHttpThrottlingMonitor http://sharepoint -Category Memory -Counter 'Available Mbytes' -IsDesc -HealthScoreBuckets $buckets
```

This example sets the Health Score bucket values for the  `Memory\Available Mbytes` counter to the array listed for the  `http://sharepoint` Web application. 
  
------------------EXAMPLE 2------------------
  
```
Set-SPWebApplicationHttpThrottlingMonitor http://sharepoint0 -Category Memory -Counter 'Available Mbytes' -IsDesc -UpperLimit 3000
```

This example sets the upper limit for the  `Memory\Available Mbytes` counter, the highest value in the Health Score buckets, to 3000 for the  `http://sharepoint` Web application. 
  
## See also

#### 

[Get-SPWebApplicationHttpThrottlingMonitor](get-spwebapplicationhttpthrottlingmonitor.md)
  
[Enable-SPWebApplicationHttpThrottling](enable-spwebapplicationhttpthrottling.md)
  
[Disable-SPWebApplicationHttpThrottling](disable-spwebapplicationhttpthrottling.md)

