---
title: "Set-SPServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2bb511f8-4179-4e0d-bbe9-51e3c9bef1c8

description: "Sets properties of a service application."
---

# Set-SPServiceApplication

Sets properties of a service application.
  
```
Set-SPServiceApplication [-Identity] <SPServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DefaultEndpoint <SPServiceEndpointPipeBind>] [-IisWebServiceApplicationPool <SPIisWebServiceApplicationPoolPipeBind>] [-ServiceApplicationProxyGroup <SPServiceApplicationProxyGroupPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Set-SPServiceApplication** cmdlet to set various properties of a service application such as the default endpoint, and the application pool used by the service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> |Specifies the service application to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a subscription settings service application (for example, SubSettingsApp1); or an instance of a valid **SPServiceApplication** object.  <br/> |
|**DefaultEndpoint** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceEndpointPipeBind  <br/> |Specifies the address of the default endpoint of the service application.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**IisWebServiceApplicationPool** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the name or identity of the application pool used by the service application.  <br/> The IisWebServiceApplicationPool parameter only applies to Web Service applications.  <br/> |
|**ServiceApplicationProxyGroup** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyGroupPipeBind  <br/> |Specifies a custom service application proxy group for the Web application to use. The Web application will use the proxies in this proxy group to connect to service applications. If the **ServiceApplicationProxyGroup** parameter is not specified, the farm's default proxy group is used.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultEndpoint** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceEndpointPipeBind  <br/> ||
|**IisWebServiceApplicationPool** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**ServiceApplicationProxyGroup** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyGroupPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------------EXAMPLE----------------
  
```
$serviceapp = Get-SPServiceApplication "My Service App"
```

```
Set-SPServiceApplication $serviceapp -DefaultEndpoint https
```

This example sets the default endpoint of the service application to be  `https`.
  
## See also

#### 

[Get-SPServiceApplication](get-spserviceapplication.md)
  
[Publish-SPServiceApplication](publish-spserviceapplication.md)
  
[Remove-SPServiceApplication](remove-spserviceapplication.md)

