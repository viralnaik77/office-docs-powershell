---
title: "Get-SPBrowserCustomerExperienceImprovementProgram"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5870288c-8713-4045-9768-114df92e5538

description: "Returns the current opt-in state for the browser Customer Experience Improvement Program."
---

# Get-SPBrowserCustomerExperienceImprovementProgram

Returns the current opt-in state for the browser Customer Experience Improvement Program.
  
```
Get-SPBrowserCustomerExperienceImprovementProgram -Farm <SwitchParameter> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Get-SPBrowserCustomerExperienceImprovementProgram** cmdlet reads the current opt-in state for the browser Customer Experience Improvement Program. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Farm** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the opt-in state for the farm is returned by this cmdlet.  <br/> |
|**SiteSubscription** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Returns the opt-in state for the specified site subscription.  <br/> The type must be a valid URL, in the form http://server_name; a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a site subscription (for example, SiteSubscription1); or an instance of a valid **SiteSubscription** object.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Returns the opt-in state for the specified SharePoint Web application.  <br/> The type must be a valid URL, in the form http://server_name; a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of SharePoint Web application (for example, MyOfficeApp1); or an instance of a valid **SPWebApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Farm** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SiteSubscription** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------------EXAMPLE 1-----------------------
  
```
Get-SPBrowserCustomerExperienceImprovementProgram -WebApplication http://WebAppexample1
```

This example returns the current Customer Experience Improvement Program opt-in state for the Web application,  `WebAppexample1`.
  
------------------EXAMPLE 2-----------------------
  
```
Get-SPSiteSubscription http://SiteSubscription1 | Get- SPBrowserCustomerExperienceImprovementProgram
```

The following example returns the Customer Experience Improvement Program opt-in state for the site subscription,  `SiteSubscription1`.
  
## See also

#### 

[Set-SPBrowserCustomerExperienceImprovementProgram](set-spbrowsercustomerexperienceimprovementprogram.md)

