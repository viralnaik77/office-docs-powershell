---
title: "Set-SPWorkflowConfig"
ms.author: kenwith
author: kenwith
manager: laurawi
ms.date: 1/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 876a4206-6c28-446e-9686-c8916c9bbfec

description: "Configures the workflow settings for the specified Web application."
---

# Set-SPWorkflowConfig

Configures the workflow settings for the specified Web application.
  
```
Set-SPWorkflowConfig -WebApplication <SPWebApplicationPipeBind> <COMMON PARAMETERS>

```

## Example

------------------EXAMPLE-----------------------
  
```
Set-SPWorkflowConfig -webapplication http://sitename -DeclarativeWorkflowsEnabled $true -EmailNoPermissionParticipantsEnabled $true -SendDocumentToExternalParticipants $false
```

This example sets the workflow settings for the specified Web application to turn on declarative workflows, turn on e-mail to participants who do not have permissions to the site, and turn off the functionality to send e-mail messages as attachments to external participants.
  
No return values. Use the **Get-SPWorkflowConfig** cmdlet to see values.To set farm-level workflow settings for event-delivery time-out and to postpone threshold and batch size, use **Set-SPFarmConfig**. 
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
Use the **Set-SPWorkflowConfig** cmdlet to configure the workflow settings for the specified Web application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SiteCollection_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the name or URL of the site collection.  <br/> The only other parameter that is used with the **SiteCollection** parameter is the **DeclarativeWorkflowsEnabled** parameter. No other parameters are used.  <br/> |
| _WebApplication_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the name or URL of the Web application.  <br/> The type must be a valid name or GUID, in the form WebApplication-1212, or a URL, in the form http://server_name/WebApplication-1212.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _DeclarativeWorkflowsEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |Sets whether declarative workflows are allowed to run in the Web application.  <br/> The type must be either **1** for **True** or **0** for **False**.  <br/> |
| _EmailNoPermissionParticipantsEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |Sets whether workflows send task e-mail messages to users who do not have permissions to the site in which the workflows are running.  <br/> The type must be either **1** for **True** or **0** for **False**.  <br/> |
| _SendDocumentToExternalParticipants_ <br/> |Optional  <br/> |System.Boolean  <br/> |Sets whether workflows automatically send a copy of the document as an e-mail attachment to participants who do not have access to the site or who are not in any linked directory other than Active Directory Domain Services (AD DS).  <br/> The type must be either **1** for **True** or **0** for **False**.  <br/> |
| _SingleWorkflowEpisodeTimeout_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies a timeout value for a single workflow event.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SiteCollection** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**DeclarativeWorkflowsEnabled** <br/> |Optional  <br/> |System.Boolean  <br/> ||
|**EmailNoPermissionParticipantsEnabled** <br/> |Optional  <br/> |System.Boolean  <br/> ||
|**SendDocumentToExternalParticipants** <br/> |Optional  <br/> |System.Boolean  <br/> ||
   
## See also

#### 

[Get-SPWorkflowConfig](get-spworkflowconfig.md)

