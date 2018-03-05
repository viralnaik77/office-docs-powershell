---
title: "New-SPContentDeploymentJob"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46faa5c0-95be-4d00-b876-ae874a1a204c

description: "Creates a content deployment job."
---

# New-SPContentDeploymentJob

Creates a content deployment job.
  
```
New-SPContentDeploymentJob -Name <String> -SPContentDeploymentPath <SPContentDeploymentPathPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Description <String>] [-EmailAddresses <String[]>] [-EmailNotifications <None | SendEmailOnFailure | SendEmailOnSuccess | SendEmailOnAlways>] [-HostingSupportEnabled <SwitchParameter>] [-IncrementalEnabled <SwitchParameter>] [-Schedule <String>] [-ScheduleEnabled <SwitchParameter>] [-Scope <SPWebPipeBind[]>] [-SqlSnapshotSetting <None | CreateNew>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
Get-SPContentDeploymentPath "Path 1" | New-SPContentDeploymentJob -Name "Deployment Job" -SPContentDeploymentPath $_ -IncrementalEnabled:$true -ScheduleEnabled:$false
```

This example creates a new content deployment job called  `Deployment Job` by using the deployment path  `Path 1`. The job is configured to be an incremental job with no schedule.
  
## Detailed Description

The **New-SPContentDeploymentJob** cmdlet adds a new content deployment job to a farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the new content deployment job.  <br/> The type must be a valid name of a content deployment job; for example, DeployJob1.  <br/> |
| _SPContentDeploymentPath_ <br/> |Required  <br/> |Microsoft.SharePoint.Publishing.Cmdlet.SPContentDeploymentPathPipeBind  <br/> |Specifies the deployment path to associate with the new deployment job.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a content deployment job (for example; DeployJob1); or an instance of a valid **SPContentDeploymentJob** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Description_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the description for the content deployment job. The name can be a maximum of 4096 alphanumeric characters.  <br/> The type must be a valid string.  <br/> |
| _EmailAddresses_ <br/> |Optional  <br/> |System.String[]  <br/> |Specifies the e-mail addresses of individuals who receive notification e-mails about this **ContentDeploymentJob** object.  <br/> The type must be a list of valid e-mail addresses.  <br/> |
| _EmailNotifications_ <br/> |Optional  <br/> |Microsoft.SharePoint.Publishing.Administration.ContentDeploymentNotificationSettings  <br/> |Specifies how e-mail notifications are sent about this **ContentDeploymentJob** object.  <br/> The type must be one of the following:  <br/> - **Never** specifies that e-mail notifications will not be sent when a job succeeds or fails.  <br/> - **SendEmailOnSuccess** specifies that e-mail notifications will be sent if a content deployment job succeeds.  <br/> - **SendEmailOnFailure** specifies that e-mail notifications will be sent if a content deployment job fails.  <br/> - **SendEmailOnAlways** specifies that e-mail notifications will be sent when a job succeeds or fails.  <br/> |
| _HostingSupportEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Enables special hosting- behavior. The default value is **False**.  <br/> Normally, a content deployment job is enabled or disabled by using the SharePoint Central Administration Web site. However, in the case of hosting, the tenant administrator does not have permissions to access the Central Administration page to configure jobs. Therefore, when the **HostingSupportEnabled** parameter is set to **True**, the hoster creates the job, so that tenants can enable or disable their deployment jobs from their tenant administration site.  <br/> |
| _IncrementalEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that only incremental changes are deployed to the destination site collection.  <br/> |
| _Schedule_ <br/> |Optional  <br/> |System.String  <br/> |Sets the schedule for the deployment job.  <br/> The type must be a valid **SPSchedule** object.  <br/> |
| _ScheduleEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies to enable the schedule for the deployment job. If the schedule is not enabled the job can be run only manually.  <br/> |
| _Scope_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind[]  <br/> |Sets the scope of the deployment job. SPSites passed in must exist in the current path of the source site collection. The default scope is the entire site collection. Valid values include an **SPWeb** object or an array of **SPWeb** objects.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint Foundation 2013 Web site (for example, MySPSite1); or an instance of a valid **SPWeb** object.  <br/> |
| _SqlSnapshotSetting_ <br/> |Optional  <br/> |Microsoft.SharePoint.Publishing.Administration.ContentDeploymentSqlSnapshotSetting  <br/> |Creates a database snapshot of the source SharePoint Foundation 2013 content database to use for the export process.  <br/> The type must be one of the following values:  <br/> - **None** <br/> - **CreateNew** <br/> > [!NOTE]> The **CreateNew** value requires that SQL Server Enterprise Edition be installed.           |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**SPContentDeploymentPath** <br/> |Required  <br/> |Microsoft.SharePoint.Publishing.Cmdlet.SPContentDeploymentPathPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Description** <br/> |Optional  <br/> |System.String  <br/> ||
|**EmailAddresses** <br/> |Optional  <br/> |System.String[]  <br/> ||
|**EmailNotifications** <br/> |Optional  <br/> |Microsoft.SharePoint.Publishing.Administration.ContentDeploymentNotificationSettings  <br/> ||
|**HostingSupportEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**IncrementalEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Schedule** <br/> |Optional  <br/> |System.String  <br/> ||
|**ScheduleEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Scope** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind[]  <br/> ||
|**SqlSnapshotSetting** <br/> |Optional  <br/> |Microsoft.SharePoint.Publishing.Administration.ContentDeploymentSqlSnapshotSetting  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPContentDeploymentJob](get-spcontentdeploymentjob.md)
  
[Remove-SPContentDeploymentJob](remove-spcontentdeploymentjob.md)
  
[Set-SPContentDeploymentJob](set-spcontentdeploymentjob.md)
  
[Start-SPContentDeploymentJob](start-spcontentdeploymentjob.md)

