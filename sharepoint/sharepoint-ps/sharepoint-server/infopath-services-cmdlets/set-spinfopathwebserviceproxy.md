---
title: "Set-SPInfoPathWebServiceProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c4e4639e-cfc0-4bf2-8f6a-de3e09c3080c

description: "Sets parameters for an existing SharePoint Web service application."
---

# Set-SPInfoPathWebServiceProxy

Sets parameters for an existing SharePoint Web service application.
  
```
Set-SPInfoPathWebServiceProxy [-Identity] <SPWebServiceProxyPipeBind> [-AllowForUserForms <String>] [-AllowWebServiceProxy <String>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPInfoPathWebServiceProxy** cmdlet configures exposed parameters for an existing SharePoint Web application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPWebServiceProxyPipeBind  <br/> |Specifies the SharePoint Web service application proxy to update.  <br/> The type must be a valid URL, in the form http://server_name; a valid name of a Web application (for example, WebApp1); a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid **SPWebServiceProxy** object.  <br/> |
|**AllowForUserForms** <br/> |Optional  <br/> |System.String  <br/> |Specifies that a form opened in the InfoPath client can use the InfoPath Forms Services Web service proxy to connect to a Web service. This parameter can be set only when **AllowWebServiceProxy** is set to **True**.  <br/> The type must be one of the following: **True**, **False** The default value is False.  <br/> |
|**AllowWebServiceProxy** <br/> |Optional  <br/> |System.String  <br/> |Specifies that browser-enabled form templates can use the InfoPath Forms Services Web service proxy to connect to a Web service.  <br/> The type must be one of the following: **True**, **False** The default value is False.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPWebServiceProxyPipeBind  <br/> ||
|**AllowForUserForms** <br/> |Optional  <br/> |System.String  <br/> ||
|**AllowWebServiceProxy** <br/> |Optional  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Set-SPInfoPathWebServiceProxy -Identity "http://server_name" -AllowWebServiceProxy $true
```

This example sets the Web service proxy for a Web application.
  
## See also

#### 

[Get-SPInfoPathWebServiceProxy](get-spinfopathwebserviceproxy.md)

