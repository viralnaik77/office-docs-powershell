---
title: "Set-SPTopologyServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46f73481-63f1-4d5c-a75c-ebe2d21d113d

description: "Sets the properties on the topology service application of the local farm."
---

# Set-SPTopologyServiceApplication

Sets the properties on the topology service application of the local farm.
  
```
Set-SPTopologyServiceApplication [-Identity] <SPTopologyWebServiceApplicationPipeBind> -LoadBalancerUrl <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPTopologyServiceApplication** cmdlet sets the advanced properties of an application when the **Identity** parameter is used. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTopologyWebServiceApplicationPipeBind  <br/> |Specifies the GUID of the application to be set.  <br/> The type must be a valid GUID, in the form 1234-456-854gh.  <br/> |
|**LoadBalancerUrl** <br/> |Required  <br/> |System.String  <br/> |Specifies an external physical load balancer.  <br/> The type must be a valid URL, in the form http://search.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPTopologyWebServiceApplicationPipeBind  <br/> ||
|**LoadBalancerUrl** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
Set-SPTopologyServiceApplication 67877d63-bff4-4521-867a-ef4979ba07ce -LoadBalancedURL "https://testurl"
```

This example sets the load-balanced URL for the topology service application.
  
The topology service application GUID is unique to every farm. You can run the **Get-SPTopologyServiceApplication** cmdlet to retrieve the GUID. 
  
## See also

#### 

[Get-SPTopologyServiceApplication](get-sptopologyserviceapplication.md)
  
[Set-SPTopologyServiceApplicationProxy](set-sptopologyserviceapplicationproxy.md)

