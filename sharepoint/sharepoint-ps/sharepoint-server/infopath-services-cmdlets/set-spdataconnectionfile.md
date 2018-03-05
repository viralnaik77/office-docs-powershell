---
title: "Set-SPDataConnectionFile"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edca60a7-2028-4141-97e1-83125306fe3f

description: "Sets properties of a data connection file."
---

# Set-SPDataConnectionFile

Sets properties of a data connection file.
  
```
Set-SPDataConnectionFile [-Identity] <SPDataConnectionFilePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Category <String>] [-Confirm [<SwitchParameter>]] [-Description <String>] [-DisplayName <String>] [-WebAccessible <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPDataConnectionFile** cmdlet sets the properties of the data connection file specified in the **Identity** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPDataConnectionFilePipeBind  <br/> |Specifies the data connection file to update.  <br/> The type must be a valid GUID, in form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a data connection file (for example, DataConnectionFileName1.udcx); or an instance of a valid **SPDataConnectionFile** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Category** <br/> |Optional  <br/> |System.String  <br/> |Sets an arbitrary category on the file which can be used to group the files. The category name can have a maximum of 255 characters.  <br/> The type must be a valid string value; for example, Category1.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Description** <br/> |Optional  <br/> |System.String  <br/> |Sets the description for the data connection file. The name can be a maximum of 4096 alphanumeric characters.  <br/> The type must be a valid string; for example, Description of my universal data connection file.  <br/> |
|**DisplayName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the display name that describes the data connection file. The name can have a maximum of 255 characters.  <br/> The type must be a valid string; for example, InfoPathUDC1.  <br/> |
|**WebAccessible** <br/> |Optional  <br/> |System.String  <br/> |Specifies that the universal data connection file can be accessed by using the Web service. If false, only the forms server can retrieve the universal data connection files internally. The default value is **False**.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPDataConnectionFilePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Category** <br/> |Optional  <br/> |System.String  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Description** <br/> |Optional  <br/> |System.String  <br/> ||
|**DisplayName** <br/> |Optional  <br/> |System.String  <br/> ||
|**WebAccessible** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Set-SPDataConnectionFile -Identity "sample.udcx" -Category "Temp"
```

This example updates the  `Category` of the specified  `.udcx` file. 
  
--------------EXAMPLE 2-----------------
  
```
Set-SPDataConnectionFile -Identity "sample.udcx" -DisplayName "NewDisplayName"
```

This example updates the  `DisplayName` of the specified  `.udcx` file. 
  
--------------EXAMPLE 3-----------------
  
```
Sample.udcx" | Set-SPDataConnectionFile -Category "Temp"
```

This example updates the  `Category` of the specified  `.udcx` file. 
  
--------------EXAMPLE 4-----------------
  
```
Get-SPDataConnectionFile | where {$_.Category -eq "Category1"}  | Set-SPDataConnectionFile -Category "Category2"
```

This example updates the  `Category` field for the collection of  `.udcx` files that are returned from a query used by the **Get-SPDataConnectionFile** cmdlet. 
  
## See also

#### 

[Get-SPDataConnectionFile](get-spdataconnectionfile.md)
  
[Install-SPDataConnectionFile](install-spdataconnectionfile.md)
  
[Uninstall-SPDataConnectionFile](uninstall-spdataconnectionfile.md)

