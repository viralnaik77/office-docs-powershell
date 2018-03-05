---
title: "Move-SPProfileManagedMetadataProperty"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ad0b82ea-cfce-4e88-9bc1-ecae82f31c0b

description: "Moves multiple-string values into a term set."
---

# Move-SPProfileManagedMetadataProperty

Moves multiple-string values into a term set.
  
```
Move-SPProfileManagedMetadataProperty -Identity <String> -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-AvailableForTagging <SwitchParameter>] [-Confirm [<SwitchParameter>]] [-TermSetName <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Move-SPProfileManagedMetadataProperty** cmdlet to move multiple-string or single-string property values into a term set that you specify. If you do not specify a term set, the values are moved into the Keywords term set. Any new values you add to the property after running the cmdlet will be moved into the term set that you specified. 
  
After a user profile application has been upgraded from Office SharePoint Server 2007, single-string and multiple-string value properties are not available for use unless the **Move-SPProfileManagedMetadataProperty** cmdlet is run to map them to term sets within Managed Metadata Service. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the profile property that needs to be migrated to the taxonomy.  <br/> |
|**ProfileServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the name of the User Profile Service Application Proxy to use.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**AvailableForTagging** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Determines whether the terms in the resulting term set can be used for Managed Metadata tagging. If a term set has more than 30,000 terms, using it for Managed Metadata tagging may lead to performance issues on the client computer. Because a majority of the profile properties may have more than 30,000 terms, the default value is **No**.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**TermSetName** <br/> |Optional  <br/> |System.String  <br/> |When specified, the term set name is created. If the **TermSetName** parameter is not specified, the property is mapped to the **Keywords** term set in Managed Metadata Service.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |System.String  <br/> ||
|**ProfileServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**AvailableForTagging** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**TermSetName** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------EXAMPLE 1------------------
  
```
Move-SPProfileManagedMetadataProperty -Identity SPS-Interests -TermSetName Interests -AvailableForTagging -ProfileServiceApplicationProxy dbc4ccf5-b245-4e0f-8696-235402f83260
```

This example moves values from the **SPS-Interests** property into a new term set called  `Interests`, and marks that term set as available for tagging.
  
---------------EXAMPLE 2------------------
  
```
Get-SPServiceApplicationProxy | ?{$_.DisplayName.Contains("User Profile Service")} | Move-SPProfileManagedMetadataProperty -Identity SPS-Interests -TermSetName Interests -AvailableForTagging
```

This example performs the same task as Example 1, but pipes the result for the **ProfileServiceApplicationProxy** parameter by using the **Get-SPServiceApplicationProxy** cmdlet. 
  

