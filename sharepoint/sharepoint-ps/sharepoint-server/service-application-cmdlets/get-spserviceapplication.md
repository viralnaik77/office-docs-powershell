---
title: "Get-SPServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 71a467dc-3b95-4b65-af93-0d0d6ebb8326

description: "Returns the specified service application."
---

# Get-SPServiceApplication

Returns the specified service application.
  
```
Get-SPServiceApplication [[-Identity] <SPServiceApplicationPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-Name <String>]
```

## Detailed Description

The **Get-SPServiceApplication** cmdlet returns the service application specified by the **Identity** parameter. If no parameter is specified, the cmdlet returns all service applications in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> |Specifies the GUID of the service application to get.  <br/> |
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the friendly name of the new usage application.The type must be a valid name of a usage application; for example, UsageApplication1.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

------------------EXAMPLE 1----------------------
  
```
Get-SPServiceApplication
```

This example returns all service applications in the farm.
  
------------------EXAMPLE 2----------------------
  
```
Get-SPServiceApplication -Identity e2c2be70-6382-4ce7-8a44-ae7dadff5597
```

This example returns the service application that has the Identity "e2c2be70-6382-4ce7-8a44-ae7dadff5597".
  
------------------EXAMPLE 3----------------------
  
```
Get-SPServiceApplication -Name AccountingServiceApp
```

This example returns the service application that has the friendly name "AccountingServiceApp".
  
> [!TIP]
> You can use either the **Identity** or the **Name** parameter but if you use both, the command will process the **Identity** first and ignore the **Name**. 
  
## See also

#### 

[Set-SPServiceApplication](set-spserviceapplication.md)
  
[Get-SPServiceApplicationProxy](get-spserviceapplicationproxy.md)

