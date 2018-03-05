---
title: "Get-SPServiceApplicationEndpoint"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea8ded59-c1b9-488b-876a-c12e66a17295

description: "Returns the endpoint of a service application."
---

# Get-SPServiceApplicationEndpoint

Returns the endpoint of a service application.
  
```
Get-SPServiceApplicationEndpoint [-Identity] <SPServiceEndpointPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Get-SPServiceApplicationEndpoint** cmdlet sets the host of a service endpoint. Use the second parameter set and do not specify the **Name** parameter to return a collection of all endpoints for the specified service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceEndpointPipeBind  <br/> |Specifies the service endpoint to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URI of an endpoint address, in the form http://sitename:8003/servicemodelsamples/service; or an instance of a valid **SPServiceEndpoint** object.  <br/> |
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> |Specifies the service application to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a subscription settings service application (for example, SubscriptionSettingsApp1); or an instance of a valid **SPServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the service application endpoint.  <br/> The type must be a valid name of an service application endpoint; for example, SvcAppEndpoint1.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceEndpointPipeBind  <br/> ||
|**ServiceApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

-------------------EXAMPLE--------------------
  
```
Get-SPServiceApplicationEndpoint -ServiceApplication "ServiceSubApp1"
```

This example returns the SPServiceEndpoint object based on the specified service application.
  
## See also

#### 

[Set-SPServiceApplicationEndpoint](set-spserviceapplicationendpoint.md)

