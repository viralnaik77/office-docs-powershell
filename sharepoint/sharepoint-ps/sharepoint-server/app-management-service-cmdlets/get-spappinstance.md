---
title: "Get-SPAppInstance"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 916ac7a1-1740-42d7-b4ee-bdf3080845fd

description: "Returns the hosting quotas for an app."
---

# Get-SPAppInstance

Returns the hosting quotas for an app.
  
```
Get-SPAppInstance -Identity <SPAppInstance> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **Get-AppInstance** cmdlet to get a collection of app instances that are installed on an **SPWeb** object. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPAppInstance  <br/> |Specifies the App instance for which to find metadata.  <br/> |
|**AppInstanceId** <br/> |Required  <br/> |System.Guid  <br/> |Specifies the App Instance ID to display.  <br/> |
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Sets the query scope to a site.  <br/> > [!NOTE]> Subsites are not included.           |
|**Web** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the **SPWeb** object  <br/> |
|**App** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPApp  <br/> |Specifies the App. This parameter returns metadata for all instances of an app.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppInstanceId** <br/> |Required  <br/> |System.Guid  <br/> ||
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPAppInstance  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**Web** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
|**App** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPApp  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-----------EXAMPLE 1-----------
  
```
$instances = Get-SPAppInstance -Web http://localhost
```

This example returns a collection if more than one app is installed on http://localhost. If only one app is installed, a single object is returned.
  
-----------EXAMPLE 2-----------
  
```
$instance = Get-SPAppInstance -AppInstanceId $instance.Id
```

This example returns the ID of an instance of an app.
  
## See also

#### 

[Uninstall-SPAppInstance](uninstall-spappinstance.md)
  
[Update-SPAppInstance](update-spappinstance.md)
#### 

[Restart-SPAppInstanceJobs](http://technet.microsoft.com/library/582e2939-1a82-47fc-b1f5-f405f37196f3.aspx)

