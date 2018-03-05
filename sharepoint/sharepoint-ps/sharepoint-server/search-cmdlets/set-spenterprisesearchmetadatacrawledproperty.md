---
title: "Set-SPEnterpriseSearchMetadataCrawledProperty"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 59540fb5-c246-4732-83c5-eecb17c9b7a1

description: "Sets the properties of a metadata crawled property."
---

# Set-SPEnterpriseSearchMetadataCrawledProperty

Sets the properties of a metadata crawled property.
  
```
Set-SPEnterpriseSearchMetadataCrawledProperty -Identity <CrawledPropertyPipeBind> -IsMappedToContents <$true | $false> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication
```

```
$crawlprop = Get-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $searchapp -Name MyCrawlProp

```

```
Set-SPEnterpriseSearchMetadataCrawledProperty -Identity $crawlprop -IsMappedToContent $true
```

This example sets the  `IsMappedToContent` parameter of the crawled property  `MyCrawlProp` to  `false` (see the example for the [New-SPEnterpriseSearchMetadataCrawledProperty](new-spenterprisesearchmetadatacrawledproperty.md) command) for the default search service application. 
  
## Detailed Description

This cmdlet updates properties of a crawled property when the search functionality is configured for the first time and after any new crawled property is added to create the rules for the crawled property. **SPEnterpriseSearchMetadataCrawledProperty** represents a crawled property in the enterprise search metadata property schema. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawledPropertyPipeBind  <br/> |Specifies the crawled property to update.  <br/> The type must be an instance of a valid CrawledProperty object.  <br/> |
| _IsMappedToContents_ <br/> |Required  <br/> |System.Boolean  <br/> |Specifies that the crawled property is mapped to managed properties. Specify **true** to map a crawled property to a managed property.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawledPropertyPipeBind  <br/> ||
|**IsMappedToContents** <br/> |Required  <br/> |System.Nullable  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchMetadataCrawledProperty](new-spenterprisesearchmetadatacrawledproperty.md)
  
[Get-SPEnterpriseSearchMetadataCrawledProperty](get-spenterprisesearchmetadatacrawledproperty.md)
#### 

[VARIANT Type Constants (http://go.microsoft.com/fwlink/p/?LinkId=143322&amp;clcid=0x409)](http://go.microsoft.com/fwlink/p/?LinkId=143322&amp;clcid=0x409)

