---
title: "Set-SPContentDeploymentJob"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dd46fa9-1110-4fd5-b890-6b0fc37dbe96

description: "Sets properties of a content deployment job."
---

# Set-SPContentDeploymentJob

Sets properties of a content deployment job.
  
```
Set-SPContentDeploymentJob -Identity <SPContentDeploymentJobPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Description <String>] [-EmailAddresses <String[]>] [-EmailNotifications <None | SendEmailOnFailure | SendEmailOnSuccess | SendEmailOnAlways>] [-HostingSupportEnabled <SwitchParameter>] [-IncrementalEnabled <SwitchParameter>] [-Name <String>] [-Schedule <String>] [-ScheduleEnabled <SwitchParameter>] [-Scope <SPWebPipeBind[]>] [-SqlSnapshotSetting <None | CreateNew>] [-WhatIf [<SwitchParameter>]]

```

## Example

-----------------EXAMPLE------------------
  
```
Get-SPContentDeploymentJob "Job 1" | Set-SPContentDeploymentJob -Schedule "hourly between 0 and 59" -ScheduleEnabled:$true
```

This example sets the deployment job called  `Job 1` to run hourly. 
  
## Detailed Description

The **Set-SPContentDeploymentJob** cmdlet sets the properties of a content deployment job. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.Publishing.Cmdlet.SPContentDeploymentJobPipeBind  <br/> |Specifies the content deployment job to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a content deployment job (for example, DeployJob1); or an instance of a valid **SPContentDeploymentJob** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Description_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the description for the content deployment job. The name can be a maximum of 4096 alphanumeric characters.  <br/> The type must be a valid string.  <br/> |
| _EmailAddresses_ <br/> |Optional  <br/> |System.String[]  <br/> |Specifies the e-mail addresses of individuals who receive notification e-mails about this **ContentDeploymentJob** object.  <br/> The type must be a list of valid e-mail addresses.  <br/> |
| _EmailNotifications_ <br/> |Optional  <br/> |Microsoft.SharePoint.Publishing.Administration.ContentDeploymentNotificationSettings  <br/> |Specifies how e-mail notifications are sent about this **ContentDeploymentJob** object.  <br/> The type must be one of the following:  <br/> - **Never** specifies that e-mail notifications will not be sent when a job succeeds or fails.  <br/> - **Success** specifies that e-mail notifications will be sent if a content deployment job succeeds.  <br/> - **Failure** specifies that e-mail notifications will be sent if a content deployment job fails.  <br/> - **Always** specifies that e-mail notifications will be sent when a job succeeds or fails.  <br/> |
| _HostingSupportEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Enables special hosting behavior. The default value is **False**.  <br/> Normally, a content deployment job is enabled or disabled by using the SharePoint Central Administration Web site. However, in the case of hosting, the tenant administrator does not have permissions to access the Central Administration page to configure jobs. Therefore, when the **HostingSupportEnabled** parameter is set to **True**, the hoster creates the job, so that tenants can enable or disable their deployment jobs from their tenant administration site.  <br/> |
| _IncrementalEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that only incremental changes are deployed to the destination site collection.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the new content deployment job.  <br/> The type must be a valid name of a content deployment job; for example, DeployJob1.  <br/> |
| _Schedule_ <br/> |Optional  <br/> |System.String  <br/> |Sets the schedule for the deployment job.  <br/> The type must be a valid **SPSchedule** object.  <br/> |
| _ScheduleEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Enables the schedule for the deployment job. If the schedule is not enabled, the job can be run manually only.  <br/> |
| _Scope_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind[]  <br/> |Sets the scope of the deployment job. **SPSite** objects that are passed in must exist in the current path of the source site collection. The default scope is the entire site collection. Valid values include a **SPWeb** object or an array of **SPWeb** objects.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint Foundation 2013 Web site (for example, MySPSite1); or an instance of a valid **SPWeb** object.  <br/> |
| _SqlSnapshotSetting_ <br/> |Optional  <br/> |Microsoft.SharePoint.Publishing.Administration.ContentDeploymentSqlSnapshotSetting  <br/> |Backs up the SharePoint Foundation 2013 content database by using SQL Server.  <br/> The type must be one of the following values: **None** or **CreateNew**.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Publishing.Cmdlet.SPContentDeploymentJobPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Description** <br/> |Optional  <br/> |System.String  <br/> ||
|**EmailAddresses** <br/> |Optional  <br/> |System.String[]  <br/> ||
|**EmailNotifications** <br/> |Optional  <br/> |Microsoft.SharePoint.Publishing.Administration.ContentDeploymentNotificationSettings  <br/> ||
|**HostingSupportEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**IncrementalEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**Schedule** <br/> |Optional  <br/> |System.String  <br/> ||
|**ScheduleEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Scope** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind[]  <br/> ||
|**SqlSnapshotSetting** <br/> |Optional  <br/> |Microsoft.SharePoint.Publishing.Administration.ContentDeploymentSqlSnapshotSetting  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPContentDeploymentPath](get-spcontentdeploymentpath.md)
  
[New-SPContentDeploymentJob](new-spcontentdeploymentjob.md)
  
[Remove-SPContentDeploymentJob](remove-spcontentdeploymentjob.md)
  
[Start-SPContentDeploymentJob](start-spcontentdeploymentjob.md)

