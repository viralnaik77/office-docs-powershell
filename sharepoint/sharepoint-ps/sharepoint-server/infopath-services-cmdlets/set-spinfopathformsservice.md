---
title: "Set-SPInfoPathFormsService"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/30/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ac13cd00-c372-4159-943d-98c016c7e96a

description: "Sets parameters for InfoPath Forms Services in SharePoint Server 2013."
---

# Set-SPInfoPathFormsService

Sets parameters for InfoPath Forms Services in SharePoint Server 2013.
  
```
Set-SPInfoPathFormsService [-ActiveSessionTimeout <Int32>] [-AllowEmbeddedSqlForDataConnections <String>] [-AllowUdcAuthenticationForDataConnections <String>] [-AllowUserFormBrowserEnabling <String>] [-AllowUserFormBrowserRendering <String>] [-AllowUserFormCrossDomainDataConnections <String>] [-AllowViewState <String>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DefaultDataConnectionTimeout <Int32>] [-Identity <SPFormsServicePipeBind>] [-MaxDataConnectionResponseSize <Int32>] [-MaxDataConnectionRoundTrip <Int32>] [-MaxDataConnectionTimeout <Int32>] [-MaxFormLoadTime <Int32>] [-MaxPostbacksPerSession <Int32>] [-MaxSizeOfUserFormState <Int32>] [-MaxUserActionsPerPostback <Int32>] [-MemoryCacheSize <Int32>] [-RequireSslForDataConnections <String>] [-ViewStateThreshold <Int32>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------------EXAMPLE 1-----------------
  
```
Set-SPInfoPathFormsService -AllowUserFormBrowserEnabling $true -AllowUserFormBrowserRendering $false
```

This example modifies the  `AllowUserFormBrowserEnabling` and  `AllowUserFormBrowserRendering` parameter values. 
  
--------------EXAMPLE 2-----------------
  
```
Set-SPInfoPathFormsService -AllowViewState $true -ViewStateThreshold 40961
```

This example modifies the  `AllowViewState` and  `ViewStateThreshold` parameter values. 
  
## Detailed Description

The **Set-SPInfoPathFormsService** cmdlet modifies the settings for InfoPath Forms Services in SharePoint Server 2013. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ActiveSessionTimeout_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the duration, in minutes, that a form's session state can remain active. The default value is **1440**.  <br/> The type must be a non-negative integer value in the range from 0 through 999,999.  <br/> |
| _AllowEmbeddedSqlForDataConnections_ <br/> |Optional  <br/> |System.String  <br/> |Specifies a value that indicates whether embedded SQL authentication can be used by browser-enabled InfoPath 2016 form templates.  <br/> The type must be one of the following values: **True**, **False** (default)  <br/> |
| _AllowUdcAuthenticationForDataConnections_ <br/> |Optional  <br/> |System.String  <br/> |Specifies that authentication information in a universal data connection (.udcx file) can be used.  <br/> The type must be one of the following values: **True** (default), **False** <br/> |
| _AllowUserFormBrowserEnabling_ <br/> |Optional  <br/> |System.String  <br/> |Specifies that users can browser enable form templates that do not contain form code, require full trust, enable rendering on a mobile device, or use a data connection managed by a server administrator.  <br/> The type must be one of the following values: **True** (default), **False** <br/> |
| _AllowUserFormBrowserRendering_ <br/> |Optional  <br/> |System.String  <br/> |Specifies that browser-enabled form templates will be rendered by InfoPath Forms Services.  <br/> The type must be one of the following values: **True** (default), **False** <br/> |
| _AllowUserFormCrossDomainDataConnections_ <br/> |Optional  <br/> |System.String  <br/> |Specifies that data connections to data sources located in a different domain can be queried.  <br/> The type must be one of the following values: **True**, **False** (default)  <br/> |
| _AllowViewState_ <br/> |Optional  <br/> |System.String  <br/> |Defines the location to store form session state: View state when **True**, or Session State Service when **False**.  <br/> The type must be one of the following values: **True**, **False** (default)  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DefaultDataConnectionTimeout_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the default data connection timeout in milliseconds. The default value is **10000** (10 seconds).  <br/> The type must be a non-negative integer and less than or equal to the value set for **MaxDataConnectionTimeout**.  <br/> |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPFormsServicePipeBind  <br/> |Specifies the InfoPath Forms Services service to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an InfoPath Forms Services service (for example, FormsService1); or an instance of a valid **SPFormsService** object.  <br/> |
| _MaxDataConnectionResponseSize_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum size allowed for a data connection response. The default value is **15000** kilobytes (KB).  <br/> The type must be a non-negative integer.  <br/> |
| _MaxDataConnectionRoundTrip_ <br/> |Optional  <br/> |System.Int32  <br/> |Sets a threshold, in milliseconds, for the maximum time it takes from the start of a data request to the return of the data request on the server (the data connection round trip). If the data connection round trip time exceeds this threshold, an event is logged in the Operational log.  <br/> |
| _MaxDataConnectionTimeout_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum data connection timeout in milliseconds. The default value is **20000** (20 seconds).  <br/> The type must be a non-negative integer and less than or equal to 999999.  <br/> |
| _MaxFormLoadTime_ <br/> |Optional  <br/> |System.Int32  <br/> |Sets a threshold, in milliseconds, for maximum form load time. If form load time exceeds this threshold, an event is logged in the Operational log.  <br/> The **MaxFormLoadTime** parameter measures the time it takes for a form to open, starting from when the request is accepted by the server until it leaves the server.  <br/> |
| _MaxPostbacksPerSession_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the value of the maximum postbacks that an instance of a browser-enabled InfoPath 2016 form template can make to the InfoPath Forms Services service. The default value is **20**.  <br/> The type must be a non-negative integer and less than or equal to 999999.  <br/> |
| _MaxSizeOfUserFormState_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum size of user form data that is allowed in the state service in bytes.  <br/> |
| _MaxUserActionsPerPostback_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum user actions per postback. The default value is **200**.  <br/> The type must be a non-negative integer and less than or equal to 999999.  <br/> |
| _MemoryCacheSize_ <br/> |Optional  <br/> |System.Int32  <br/> |Sets the size, in megabytes (MB), of the cache for solutions in memory.  <br/> The default value is 250 MB.  <br/> |
| _RequireSslForDataConnections_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the Secure Sockets Layer (SSL) requirement value. If data connections in browser-enabled form templates require basic authentication or digest authentication, a password is sent over the network. Set this value to **True** to require an SSL-encrypted connection for these authentication types.  <br/> The type must be one of the following values: **True** (default), **False**.  <br/> |
| _ViewStateThreshold_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum size in kilobytes of the session state when stored in the form view. The default value is **40**.  <br/> The type must be a non-negative integer and less than or equal to 99,999,999.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**MaxSizeOfFormSessionState** <br/> |Optional  <br/> |System.Nullable  <br/> |Specifies the value of the maximum size in kilobytes of session state an instance of a browser-enabled InfoPath form template can use. The default value is **4096**.  <br/> The type must be a non-negative integer and less than or equal to 999999.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ActiveSessionTimeout** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**AllowEmbeddedSqlForDataConnections** <br/> |Optional  <br/> |System.String  <br/> ||
|**AllowUdcAuthenticationForDataConnections** <br/> |Optional  <br/> |System.String  <br/> ||
|**AllowUserFormBrowserEnabling** <br/> |Optional  <br/> |System.String  <br/> ||
|**AllowUserFormBrowserRendering** <br/> |Optional  <br/> |System.String  <br/> ||
|**AllowUserFormCrossDomainDataConnections** <br/> |Optional  <br/> |System.String  <br/> ||
|**AllowViewState** <br/> |Optional  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultDataConnectionTimeout** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPFormsServicePipeBind  <br/> ||
|**MaxDataConnectionResponseSize** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaxDataConnectionRoundTrip** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaxDataConnectionTimeout** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaxFormLoadTime** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaxPostbacksPerSession** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaxSizeOfUserFormState** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaxUserActionsPerPostback** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MemoryCacheSize** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**RequireSslForDataConnections** <br/> |Optional  <br/> |System.String  <br/> ||
|**ViewStateThreshold** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPInfoPathFormsService](get-spinfopathformsservice.md)

