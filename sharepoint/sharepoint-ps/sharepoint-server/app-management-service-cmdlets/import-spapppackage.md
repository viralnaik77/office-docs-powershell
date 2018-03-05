---
title: "Import-SPAppPackage"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: be0c922a-ec67-484e-bf55-37b7ab94c624

description: "Imports an app package."
---

# Import-SPAppPackage

Imports an app package.
  
```
Import-SPAppPackage -Path <String> -Site <SPSitePipeBind> -Source <InvalidSource | Marketplace | CorporateCatalog | DeveloperSite | ObjectModel | RemoteObjectModel> [-AssetId <String>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-ContentMarket <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Import-SPAppPackage** cmdlet to import an app package from the content database and create an app inside the site collection by using the **SiteCollection** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies the path of the input file.  <br/> |
|**SiteCollection** <br/> |Required  <br/> |Microsoft.SharePoint.SPSite  <br/> |Sets the scope of the location of the imported app package. Valid value is: Site collection.  <br/> |
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the **SPSite** object to import.  <br/> |
|**Source** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPAppSource  <br/> |Defines the source of the app.  <br/> The following are valid values:  <br/> -- **SharePoint Store** <br/> -- **App catalog** <br/> -- **SharePointService** - Indicates apps that were built in place with SharePoint features, for example Access Services.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**AssetId** <br/> |Optional  <br/> |System.String  <br/> |Specifies the Asset Id to import.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**ContentMarket** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the content market.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**Source** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPAppSource  <br/> ||
|**AssetId** <br/> |Optional  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ContentMarket** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------EXAMPLE---------- 
  
```
$spapp = Import-SPAppPackage -Path .\feature-upgrade-v1.spapp -Site http://localhost -Source ([microsoft.sharepoint.administration.spappsource]::ObjectModel)
```

This example imports an app package.
  
## See also

#### 

[Export-SPAppPackage](export-spapppackage.md)

