---
title: "Get-SPWebApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11d6521f-f99c-433e-9ab5-7cf9e953457a

description: "Returns all Web applications that match the given criteria."
---

# Get-SPWebApplication

Returns all Web applications that match the given criteria.
  
```
Get-SPWebApplication [[-Identity] <SPWebApplicationPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-IncludeCentralAdministration <SwitchParameter>]
```

## Detailed Description

The **Get-SPWebApplication** cmdlet returns all Web applications that match the scope given by the **Identity** parameter. The **Identity** can be the name of the name, URL, or GUID of the Web application. If no **Identity** is specified, all Web applications are returned. 
  
The Central Administration Web application is only returned if its exact identity is provided or the **IncludeCentralAdministration** flag is provided. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the name, URL, or GUID of the Web application.  <br/> The type must be a valid URL, in the form http://server_name; a GUID, in the form 1234-5678-9876-0987; or a valid name, in the form SPWebApplication - 1212.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**IncludeCentralAdministration** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Includes the Central Administration Web application in the collection of Web applications that can be returned. The **IncludeCentral Administration** parameter must still meet any other filters provided.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**IncludeCentralAdministration** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1----------------------
  
```
$w = Get-SPWebApplication http://sitename
```

This example gets the Web application for  `http://sitename` and stores it in a variable. 
  
------------------EXAMPLE 2-----------------------
  
```
Get-SPWebApplication -IncludeCentralAdministration | Where { $_.DefaultServerComment -eq "SharePoint Central Administration v4"} | Format-List *
```

This example displays all public properties on the  `SharePoint Central Administration` Web application in list format. 
  
## See also

#### 

[Get-SPWebApplicationHttpThrottlingMonitor](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/performance-cmdlets/get-spwebapplicationhttpthrottlingmonitor.md)

