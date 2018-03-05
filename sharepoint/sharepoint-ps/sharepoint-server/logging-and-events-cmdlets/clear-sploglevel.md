---
title: "Clear-SPLogLevel"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c2f3ba1c-8ead-459e-82bd-f8aeb71f6709

description: "Resets the Windows trace logging and event logging levels to their default values."
---

# Clear-SPLogLevel

Resets the Windows trace logging and event logging levels to their default values.
  
```
Clear-SPLogLevel [-AssignmentCollection <SPAssignmentCollection>] [-Identity <String[]>] [-InputObject <PSObject>]
```

## Detailed Description

The **Clear-SPLogLevel** cmdlet resets the Windows event logging and trace logging levels for the specified categories to the default values. If the **Identity** parameter is not provided, all categories are affected. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Identity** <br/> |Optional  <br/> |System.String[]  <br/> |Specifies the name(s) of the category or set of categories to set the throttle for; for example, "Unified Logging Service". If the **Identity** parameter is not specified, the event throttling setting is applied to all categories in the farm.  <br/> Providing an invalid category is a non-terminating error and will be ignored.  <br/> |
|**InputObject** <br/> |Optional  <br/> |System.Management.Automation.PSObject  <br/> |Specifies the result of the **InputObject** parameter to be piped. The value can be a string in a format identical to the **Identity** parameter, or can be an **SPDiagnosticsCategory** object. The user can retrieve one or more categories from the **Get-SPLogLevel** cmdlet, modify their values, and then pipe the results to the **Set-SPLogLevel** cmdlet.  <br/> |
   
## Example

--------------EXAMPLE 1-----------------
  
```
Clear-SPLogLevel -Identity Cat1
```

This example resets the log levels for a single category.
  
--------------EXAMPLE 2-----------------
  
```
"Cat1", "Cat2", "Cat3" | Clear-SPLogLevel
```

This example resets the log levels for multiple categories.
  
--------------EXAMPLE 3-----------------
  
```
Get-SPLogLevel | Clear-SPLogLevel
```

This example resets the log levels for all categories.
  
## See also

#### 

[Get-SPLogLevel](get-sploglevel.md)
  
[Set-SPLogLevel](set-sploglevel.md)

