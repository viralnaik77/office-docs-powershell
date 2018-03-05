---
title: "Set-SPTranslationServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4632f359-9cb0-4d69-87fc-6ad19a95966d

description: "Sets property settings on a Machine Translation service application."
---

# Set-SPTranslationServiceApplication

Sets property settings on a Machine Translation service application.
  
```
Set-SPTranslationServiceApplication -Identity <TranslationServiceApplicationPipeBind> [-AddEnabledFileExtensions <String[]>] [-ApplicationPool <SPIisWebServiceApplicationPoolPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-ClearEnabledFileExtensions <SwitchParameter>] [-Confirm [<SwitchParameter>]] [-DatabaseCredential <PSCredential>] [-DatabaseName <String>] [-DatabaseServer <String>] [-DisableBinaryFileScan <$true | $false>] [-EnableAllFileExtensions <SwitchParameter>] [-FailoverDatabaseServer <String>] [-JobExpirationDays <Int32>] [-KeepAliveTimeout <Int32>] [-MachineTranslationAddress <String>] [-MachineTranslationCategory <String>] [-MachineTranslationClientId <String>] [-MaximumBinaryFileSize <Int32>] [-MaximumItemsPerDay <Int32>] [-MaximumItemsPerPartitionPerDay <Int32>] [-MaximumSyncTranslationRequests <Int32>] [-MaximumTextFileSize <Int32>] [-MaximumTranslationAttempts <Int32>] [-MaximumTranslationTime <Int32>] [-MaximumWordCharacterCount <Int32>] [-RecycleProcessThreshold <Int32>] [-RemoveEnabledFileExtensions <String[]>] [-TimerJobFrequency <Int32>] [-TotalActiveProcesses <Int32>] [-TranslationsPerInstance <Int32>] [-UseDefaultInternetSettings <SwitchParameter>] [-WebProxyAddress <String>] [-WhatIf [<SwitchParameter>]]

```

## Example

---------------EXAMPLE---------------
  
```
Set-SPTranslationServiceApplication TranslationService -JobExpirationDays 14 -TotalActiveProcesses 3
```

This example sets the job expiration to 14 days and the number of worker processes per server to 3 for the Machine Translation Service application named TranslationService.
  
## Detailed Description

Use the **Set-SPTranslationServiceApplication** cmdlet to set properties on a Machine Translation service application in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.TranslationServices.Powershell.TranslationServiceApplicationPipeBind  <br/> |Specifies the URL or GUID of the instance of the Machine Translation service to set.  <br/> The type must be a valid URL in the form, http://server_name or a valid GUID (for example, 12345678-90ab-cdef-1234-567890bcdefgh).  <br/> |
| _AddEnabledFileExtensions_ <br/> |Optional  <br/> |System.String[]  <br/> |Comma delimited list of file extensions that you want to add to the set of enabled file extensions for the Machine Translation Service application  <br/> To return a list of supported file extensions, type [Microsoft.Office.TranslationServices.TranslationService]::EnumerateFileExtensions().  <br/> |
| _ApplicationPool_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the managed application pool that the instance of Translation Service will run in.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _ClearEnabledFileExtensions_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Disables all file extensions for the Machine Translation Service application.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseCredential_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the SQL Server credentials used for this Translation Service instance. This parameter to be used only used for SQL authentication; if not present, Windows authentication is used instead.  <br/> |
| _DatabaseName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the database name which is to be used for this Translation Service instance.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the database server which is to be used for this Translation Service instance.  <br/> |
| _DisableBinaryFileScan_ <br/> |Optional  <br/> |System.Boolean  <br/> |Determines whether Gatekeeper is run on binary files.  <br/> |
| _EnableAllFileExtensions_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Enables all file extensions for the Machine Translation Service application.  <br/> |
| _FailoverDatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the SQL server instance that will be used as a backup to the primary SQL Server instance.  <br/> |
| _JobExpirationDays_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the amount of days after which completed jobs can be automatically removed from the Machine Translation Service queue database.  <br/> |
| _KeepAliveTimeout_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the length of time (in seconds) that the worker can be inactive before it is automatically stopped.  <br/> The valid values are 60 to 600. The default value is 60.  <br/> |
| _MachineTranslationAddress_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the service URL the service application will use to call the translation provider. For example, https://api.microsofttranslator.com/v2/soap.svc  <br/> |
| _MachineTranslationCategory_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the category which will be used by the service when calling the translation provider.  <br/> |
| _MachineTranslationClientId_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the AppId which will be used by the service when calling the translation provider.  <br/> |
| _MaximumBinaryFileSize_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum file size in kilobytes (KB) which can be translated for file types which contain binary data. The valid values are 100 to 524288. The default value is 51200.  <br/> |
| _MaximumItemsPerDay_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of items which can be added to the job queue in a 24-hour period. A value of zero indicates no limit.  <br/> The valid values are 100 to 1000000. A value of zero indicates no limit. The default value is zero.  <br/> |
| _MaximumItemsPerPartitionPerDay_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of items which can be added to the job queue in a 24-hour period per partition. A value of zero indicates no limit.  <br/> The valid values are 100 to 1000000. A value of zero indicates no limit. The default value is zero.  <br/> |
| _MaximumSyncTranslationRequests_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of items which can be added to the sync queue. A valid of zero indicates no limit.  <br/> The valid values are 0 to 300. The default value is 25.  <br/> |
| _MaximumTextFileSize_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum file size in kilobytes (KB) which can be translated for file types which contain mostly text data. The valid values are 100 to 15360. The default value is 5120.  <br/> |
| _MaximumTranslationAttempts_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of attempts an unsuccessful job is tried before it is marked as Failed.  <br/> The valid values are 1 to 10. The default value is 2.  <br/> |
| _MaximumTranslationTime_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum length of time (in minutes) that a translation can take.  <br/> The valid values are 60 to 3600. The default value is 600.  <br/> |
| _MaximumWordCharacterCount_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum character count for a Microsoft Word document which can be translated.  <br/> The valid Int values are 10000 to 10000000. The default value is 500000.  <br/> |
| _RecycleProcessThreshold_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of documents which are translated before a Translation Worker process is recycled.  <br/> The valid values are 1 to 1,000. The default value is 100.  <br/> |
| _RemoveEnabledFileExtensions_ <br/> |Optional  <br/> |System.String[]  <br/> |Comma delimited list of file extensions that you want to remove from the set of enabled file extensions for the Machine Translation Service application.  <br/> To return a list of supported file extensions, type [Microsoft.Office.TranslationServices.TranslationService]::EnumerateFileExtensions().  <br/> |
| _TimerJobFrequency_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the frequency (in minutes) with which the timer job for this service application runs. The valid values are 1 to 59. The default value is 15 minutes.  <br/> |
| _TotalActiveProcesses_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of Translation Workers which are simultaneously running on a single machine.  <br/> The valid values are 1 to 5. The default value is 1.  <br/> |
| _TranslationsPerInstance_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of translations dispatched to each service instance every time the timer job is run.  <br/> Valid values are 1 to 1,000. The default value is 200.  <br/> |
| _UseDefaultInternetSettings_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Determines whether the service application will use default Internet settings for the user service account to connect to the translation provider.  <br/> |
| _WebProxyAddress_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the web proxy address and port that the service application will use to connect to the translation provider.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.TranslationServices.Powershell.TranslationServiceApplicationPipeBind  <br/> ||
|**AddEnabledFileExtensions** <br/> |Optional  <br/> |System.String[]  <br/> ||
|**ApplicationPool** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**ClearEnabledFileExtensions** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseCredential** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**DisableBinaryFileScan** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**EnableAllFileExtensions** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**FailoverDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**JobExpirationDays** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**KeepAliveTimeout** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MachineTranslationAddress** <br/> |Optional  <br/> |System.String  <br/> ||
|**MachineTranslationCategory** <br/> |Optional  <br/> |System.String  <br/> ||
|**MachineTranslationClientId** <br/> |Optional  <br/> |System.String  <br/> ||
|**MaximumBinaryFileSize** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaximumItemsPerDay** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaximumItemsPerPartitionPerDay** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaximumSyncTranslationRequests** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaximumTextFileSize** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaximumTranslationAttempts** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaximumTranslationTime** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaximumWordCharacterCount** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**RecycleProcessThreshold** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**RemoveEnabledFileExtensions** <br/> |Optional  <br/> |System.String[]  <br/> ||
|**TimerJobFrequency** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**TotalActiveProcesses** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**TranslationsPerInstance** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**UseDefaultInternetSettings** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WebProxyAddress** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPTranslationServiceApplication](new-sptranslationserviceapplication.md)
  
[New-SPTranslationServiceApplicationProxy](new-sptranslationserviceapplicationproxy.md)
  
[Set-SPTranslationServiceApplicationProxy](set-sptranslationserviceapplicationproxy.md)

