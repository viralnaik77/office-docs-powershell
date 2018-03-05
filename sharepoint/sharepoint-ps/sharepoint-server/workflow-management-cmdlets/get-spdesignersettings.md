---
title: "Get-SPDesignerSettings"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eab05628-3dba-4081-adbd-0deceeb47db0

description: "Displays SharePoint Designer 2013 features."
---

# Get-SPDesignerSettings

Displays SharePoint Designer 2013 features.
  
```
Get-SPDesignerSettings [-WebApplication] <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPDesignerSettings** cmdlet determines whether SharePoint Designer 2013 features are enabled on the specified Web application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the Web application in which the settings apply.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## Example

---------------------EXAMPLE------------------------ 
  
```
Get-SPDesignerSettings -webapplication http://contoso
```

This example retrieves the SharePoint Designer 2013 settings for the Web application,  `http://contoso`.
  
## See also

#### 

[Set-SPDesignerSettings](set-spdesignersettings.md)

