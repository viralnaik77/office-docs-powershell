---
title: "Set-SPVisioExternalData"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96bcce29-2d5b-43d7-8e09-eab1c698c454

description: "Configures settings related to external data connections for a Visio Services application."
---

# Set-SPVisioExternalData

Configures settings related to external data connections for a Visio Services application.
  
```
Set-SPVisioExternalData -UnattendedServiceAccountApplicationID <String> -VisioServiceApplication <SPVisioServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Set-SPVisioExternalData** cmdlet sets and configures settings for external data connections for the Visio Services application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**UnattendedServiceAccountApplicationID** <br/> |Required  <br/> |System.String  <br/> |Specifies the target application ID in the registered secure store service that is used to reference unattended service account credentials. The unattended service account is a single account that all documents can use to refresh data. It is required when connecting to external data sources.  <br/> The type must be a valid value less than or equal to 256 characters. The application ID must be registered in the secure store service application or an error message will be displayed.  <br/> |
|**VisioServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> |Specifies the Visio Services application that contains the **SPVisioExternalData** object.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a Visio Services application (for example, MyVisioService1); or an instance of a valid **SPVisioServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**UnattendedServiceAccountApplicationID** <br/> |Required  <br/> |System.String  <br/> ||
|**VisioServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------------EXAMPLE----------------------- 
  
```
Set-SPVisioExternalData -VisioServiceApplication "VGS1" -UnattendedServiceAccountApplicationID "SSSApp1"
```

This example sets the unattended service account application ID to  `SSSApp1` for the Visio Services application named  `VGS1`.
  
## See also

#### 

[Get-SPVisioExternalData](get-spvisioexternaldata.md)

