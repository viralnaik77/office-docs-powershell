---
title: "Set-SPPerformancePointSecureDataValues"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 784ac0d5-4706-493d-9ef5-222cbd49ec57

description: "Sets global settings for the unattended service account."
---

# Set-SPPerformancePointSecureDataValues

Sets global settings for the unattended service account.
  
```
Set-SPPerformancePointSecureDataValues [-ServiceApplication] <SPPerformancePointMonitoringServiceApplicationPipeBind> -DataSourceUnattendedServiceAccount <PSCredential> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPPerformancePointSecureDataValues** cmdlet sets global settings and properties for the unattended service account. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|||||
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.PerformancePoint.Scorecards.SPPerformancePointMonitoringServiceApplicationPipeBind  <br/> |Specifies the PerformancePoint Service application that is to be configured.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a PerformancePoint Service application (for example, PerfPointApp1); or an instance of a valid **SPPerformancePointServiceApplication** object.  <br/> |
|**DataSourceUnattendedServiceAccount** <br/> |Required  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the user credentials (user name and password) for the data source of the unattended service account.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.PerformancePoint.Scorecards.SPPerformancePointMonitoringServiceApplicationPipeBind  <br/> ||
|**DataSourceUnattendedServiceAccount** <br/> |Required  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------------EXAMPLE 1--------------------
  
```
Set-SPPerformancePointSecureDataValues -ServiceApplication "PerformancePoint Service Application" -DataSourceUnattendedServiceAccount (get-credential)
```

This example shows how to set the unattended service account by prompting the user for the user name and password.
  
--------------------EXAMPLE 2--------------------
  
```
Set-SPPerformancePointSecureDataValues -ServiceApplication "PerformancePoint Service Application" -DataSourceUnattendedServiceAccount (New-Object System.Management.Automation.PSCredential "domain\user", (ConvertTo-SecureString "password" -AsPlainText -Force))
```

This example shows how to pass the user name and password as parameters to the cmdlet.
  
The  `DataSourceUnattendedServiceAccount` parameter accepts a  `PSCredential` object. Therefore, to pass in this value as a parameter, a new  `PSCredential` object must be created using the desired username and password values. The  `PSCredential` object requires that the password be given as a  `SecureString` type. 
  

