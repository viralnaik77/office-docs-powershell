---
title: "Get-SPSecureStoreApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 23d0482f-4693-4b3d-b05a-40ce4318839d

description: "Returns a Secure Store application."
---

# Get-SPSecureStoreApplication

Returns a Secure Store application.
  
```
Get-SPSecureStoreApplication -Name <String> -ServiceContext <SPServiceContextPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Get-SPSecureStoreApplication** cmdlet returns a Secure Store application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the Secure Store application to get.  <br/> |
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context for the local Secure Store application to connect to.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**All** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------------EXAMPLE 1------------------
  
```
$ssApp = Get-SPSecureStoreApplication -ServiceContext http://contoso -Name "ContosoTargetApplication"
```

This example gets the Secure Store application for the target application with the name  `ContosoTargetApplication`.
  
------------------EXAMPLE 2------------------
  
```
Get-SPSecureStoreApplication -ServiceContext http://contoso -All
```

This example returns all of the Secure Store applications `http://contoso`.
  
## See also

#### 

[New-SPSecureStoreApplication](new-spsecurestoreapplication.md)
  
[Set-SPSecureStoreApplication](set-spsecurestoreapplication.md)
  
[Remove-SPSecureStoreApplication](remove-spsecurestoreapplication.md)
  
[Update-SPSecureStoreApplicationServerKey](update-spsecurestoreapplicationserverkey.md)

