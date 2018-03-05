---
title: "Start-SPDiagnosticsSession"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d6ba0452-de14-4268-8cec-c71eb5ea76b4

description: "Starts a diagnostic session to report diagnostic information to the usage database."
---

# Start-SPDiagnosticsSession

Starts a diagnostic session to report diagnostic information to the usage database.
  
```
Start-SPDiagnosticsSession [-AssignmentCollection <SPAssignmentCollection>] [-CorrelationId <Guid>] [-Dashboard <SwitchParameter>] [-TraceLevel <String>]
```

## Detailed Description

Use the **Start-SPDiagnosticsSession** cmdlet to report diagnostic information to the usage database. After a diagnostic session starts, all Microsoft PowerShell for SharePoint cmdlets in Microsoft PowerShell scripts will use the same correlation to report diagnostic information. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CorrelationId** <br/> |Optional  <br/> |System.Guid  <br/> |Specifies the correlation ID to be used for the diagnostic session.  <br/> |
|**Dashboard** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that diagnostics behave as if the developer dashboard were enabled.  <br/> |
|**TraceLevel** <br/> |Optional  <br/> |System.String  <br/> | Specifies the Unified Logging Service (ULS) trace level override.  <br/> **High** <br/> **Medium** <br/> **Monitorable** <br/> **Unexpected** <br/> **Verbose** <br/> **VerboseEx** <br/> **None** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CorrelationId** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**Dashboard** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**TraceLevel** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

-------------EXAMPLE-------
  
```
$correlationId = [guid]::NewGuid()
```

```
Start-SPDiagnosticsSession -CorrelationId $correlationId -Dashboard:$true -TraceLevel Verbose
```

This example starts a diagnostic session for a specified correlation ID with the trace level of verbose.
  
## See also

#### 

[Stop-SPDiagnosticsSession](stop-spdiagnosticssession.md)

