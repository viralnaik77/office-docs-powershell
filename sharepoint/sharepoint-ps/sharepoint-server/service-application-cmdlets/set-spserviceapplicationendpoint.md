---
title: "Set-SPServiceApplicationEndpoint"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d3ec1dcc-dbba-427e-b5f8-b3634db46db5

description: "Sets the host of an endpoint for a service application."
---

# Set-SPServiceApplicationEndpoint

Sets the host of an endpoint for a service application.
  
```
Set-SPServiceApplicationEndpoint [-Identity] <SPServiceEndpointPipeBind> -HostName <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Set- SPServiceApplicationEndpoint** cmdlet sets the host of a service endpoint. Use the second parameter set to reset the host of the service endpoint to use the default endpoint. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceEndpointPipeBind  <br/> |Specifies the service endpoint to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URI of an endpoint address, in the form http://sitename:8003/servicemodelsamples/service; or an instance of a valid **SPServiceEndpoint** object.  <br/> |
|**HostName** <br/> |Required  <br/> |System.String  <br/> |Specifies the default host of the service endpoint.  <br/> The type must be a valid full load balanced URL, in the form http://server_name.  <br/> |
|**ResetHostName** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Removes the current host of the service endpoint and uses the default host.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceEndpointPipeBind  <br/> ||
|**HostName** <br/> |Required  <br/> |System.String  <br/> ||
|**ResetHostName** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------------EXAMPLE-------------------
  
```
Set-SPServiceApplicationEndpoint -Identity "ServiceApp1" -HostName http://sitename -ResetHostName $true
```

This example associates the SPServiceEndpoint object with the specified identity and resets the hostname.
  
## See also

#### 

[Get-SPServiceApplicationEndpoint](get-spserviceapplicationendpoint.md)

