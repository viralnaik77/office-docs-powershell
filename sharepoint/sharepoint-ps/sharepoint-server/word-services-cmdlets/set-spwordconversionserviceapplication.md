---
title: "Set-SPWordConversionServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/21/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee2844c6-e0b9-480d-83c7-5cac9a8f293e

description: "Sets properties of a Word Automation Services application."
---

# Set-SPWordConversionServiceApplication

Sets properties of a Word Automation Services application.
  
```
Set-SPWordConversionServiceApplication -Identity <WordServiceApplicationPipeBind> [-ActiveProcesses <Int32>] [-AddSupportedFormats <String[]>] [-ApplicationPool <SPIisWebServiceApplicationPoolPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-ClearSupportedFormats <SwitchParameter>] [-Confirm [<SwitchParameter>]] [-ConversionsPerInstance <Int32>] [-ConversionTimeout <Int32>] [-DatabaseCredential <PSCredential>] [-DatabaseName <String>] [-DatabaseServer <String>] [-DisableBinaryFileScan <SwitchParameter>] [-DisableEmbeddedFonts <SwitchParameter>] [-KeepAliveTimeout <Int32>] [-MaximumConversionAttempts <Int32>] [-MaximumConversionTime <Int32>] [-MaximumGroupSize <Int32>] [-MaximumMemoryUsage <Int32>] [-MaximumSyncConversionRequests <Int32>] [-RecycleProcessThreshold <Int32>] [-RemoveSupportedFormats <String[]>] [-TimerJobFrequency <Int32>] [-WhatIf [<SwitchParameter>]]

```

## Example

-----------EXAMPLE-----------------
  
```
Get-SPServiceApplication -Name WordServices1 | Set-SPWordConversionServiceApplication -TimerJobFrequency 30
```

This example sets the timer job frequency of the  `WordServices1` application to  `30` minutes. 
  
## Detailed Description

The **Set-SPWordConversionServiceApplication** cmdlet sets global properties of a Word Automation Services application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Word.Server.Powershell.WordServiceApplicationPipeBind  <br/> |Specifies the Word Automation Services application to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a Word Automation Services application (for example, WordSvcApp1); or an instance of a valid **SPServiceApplication** object.  <br/> |
| _ActiveProcesses_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of conversion processes on each machine on which the service application runs. This value is equivalent to the number of simultaneous conversions. The default value is **8**.  <br/> The type must be a valid integer in the range from 1 to 1000.  <br/> |
| _AddSupportedFormats_ <br/> |Optional  <br/> |System.String[]  <br/> |Specifies a set of file formats to be enabled for use by the service application.  <br/> The value must be a comma-delimited list of one or more of the following: **docx**, **doc**, **mht**, **rtf**, **xml**.  <br/> |
| _ApplicationPool_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the existing IIS managed application pool in which this instance of Word Automation Services runs.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an application pool (for example, AppPoolName1); or an instance of a valid **IISWebServiceApplicationPool** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _ClearSupportedFormats_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that all file formats should be disabled for use by the service application.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _ConversionsPerInstance_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of items sent to each conversion process (see the **ActiveProcesses** parameter description earlier in this table) every time the timer job is run. The default value is **12**.  <br/> The type must be a valid integer.  <br/> |
| _ConversionTimeout_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the time, in minutes, after which a conversion that is marked InProgress is confirmed to be still running each time the timer job runs and, if necessary, the conversion is restarted. The default value is **5**.  <br/> The type must be a valid integer in the range from 1 to 60.  <br/> |
| _DatabaseCredential_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the credentials to use for connecting to the database for the Word Automation Services application. Use this parameter only if SQL Authentication is used to access the service application database.  <br/> When the **DatabaseCredential** parameter is specified, the **DatabaseName** and **DatabaseServer** parameters are required.  <br/> |
| _DatabaseName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the database to use for this instance of the Word Automation Services application.  <br/> The type must be a valid SQL database name; for example, MetadataDB1.  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the host server for the Word Automation Services database.  <br/> The type must be a valid SQL database server host name; for example, SQLServerHost1.  <br/> |
| _DisableBinaryFileScan_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether additional checks are run when Word 97 to Word 2003 documents are processed. Turn this setting off only if all documents processed by the service are trusted.  <br/> |
| _DisableEmbeddedFonts_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether embedded fonts are ignored when present in input documents.  <br/> |
| _KeepAliveTimeout_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the length of time, in seconds, that a conversion can be non-responsive before it is terminated. The default value is **30**.  <br/> The type must be a valid integer in the range from 10 to 60.  <br/> |
| _MaximumConversionAttempts_ <br/> |Optional  <br/> |System.Int32  <br/> |The maximum number of conversion attempts before a conversion is marked with status "Failed". The default value is **2**.  <br/> The type must be a valid integer in the range from 1 to 10.  <br/> |
| _MaximumConversionTime_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum length of time, in seconds, that a conversion can run before it is terminated. The default value is **300**.  <br/> The type must be a valid integer in the range from 60 to MaxInt.  <br/> |
| _MaximumGroupSize_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum size of a single group of items in bytes which is transferred in a single WCF call.  <br/> |
| _MaximumMemoryUsage_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum percentage of system memory which can be used by the service application. The default value is **100**.  <br/> The type must be a valid integer in the range from 10 to 100.  <br/> |
| _MaximumSyncConversionRequests_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the max number of sync conversion requests that can be processed at a time on each server available to the service application.  <br/> The default value is 25.  <br/> |
| _RecycleProcessThreshold_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of documents which are converted before a conversion process is recycled. For additional information about the conversion process, see the **ActiveProcess** parameter description earlier in this table.  <br/> The type must be a valid integer in the range from 1 to 1000.  <br/> |
| _RemoveSupportedFormats_ <br/> |Optional  <br/> |System.String[]  <br/> |Specifies a set of file formats to be disabled for use by the service application.  <br/> The value must be a comma delimited list of one or more of the following: **docx**, **doc**, **mht**, **rtf**, **xml**.  <br/> |
| _TimerJobFrequency_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the frequency, in minutes, with which the timer job for this service application runs. The default value is **15**.  <br/> The type must be a valid integer in the range from 1 to 59.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Word.Server.Powershell.WordServiceApplicationPipeBind  <br/> ||
|**ActiveProcesses** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**AddSupportedFormats** <br/> |Optional  <br/> |System.String[]  <br/> ||
|**ApplicationPool** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**ClearSupportedFormats** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ConversionsPerInstance** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**ConversionTimeout** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**DatabaseCredential** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**DatabaseName** <br/> |Optional  <br/> |System.String  <br/> ||
|**DatabaseServer** <br/> |Optional  <br/> |System.String  <br/> ||
|**DisableBinaryFileScan** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DisableEmbeddedFonts** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**KeepAliveTimeout** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaximumConversionAttempts** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaximumConversionTime** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaximumGroupSize** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaximumMemoryUsage** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**RecycleProcessThreshold** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**RemoveSupportedFormats** <br/> |Optional  <br/> |System.String[]  <br/> ||
|**TimerJobFrequency** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPWordConversionServiceApplication](new-spwordconversionserviceapplication.md)

