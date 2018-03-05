---
title: "Set-SPAuthenticationRealm"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d3d60059-4883-4591-a3a7-d3002c999e68

description: "Sets the authentication realm ID."
---

# Set-SPAuthenticationRealm

Sets the authentication realm ID.
  
```
Set-SPAuthenticationRealm [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Realm <String>] [-ServiceContext <SPServiceContextPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

> [!CAUTION]
> Setting a new authentication realm blocks access for all SharePoint apps that use access tokens. These access tokens reference a token issuer whose ID includes the realm ID. When the realm ID is changed, tokens from that issuer are no longer valid in the realm. So, a new token issuer must be created whose ID includes the new realm ID. Another option is for you to set the realm ID back to its previous value by using the **-Realm** parameter and specifying the previous realm ID. > Before changing the realm ID be sure to record the current realm ID so that you can set it back if needed. > This command is typically used in an environment where site subscriptions have been set up and where the owners of one site subscription want to grant access to one or more SharePoint apps but the owners of other site subscriptions do not want to grant access to that same set of apps. Giving different realm IDs to the site subscriptions makes it possible to have separate token issuers for the site subscriptions. Apps that use tokens from one issuer cannot access websites within other site subscriptions. > For more information about realm and app authentication, see [Guidelines for using certificates in high-trust apps for SharePoint 2013](https://msdn.microsoft.com/en-us/library/office/jj945118.aspx). 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Realm** <br/> |Required  <br/> |System.String  <br/> |Specifies the realm ID value to be used. This is a string presentation of a GUID.  <br/> > [!IMPORTANT]> If no value is specified, the cmdlet will fail and no error message will be displayed.           |
|**ServiceContext** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |The full URL of a site in the site subscription.  <br/> > [!IMPORTANT]> If the specified URL is a part of a site subscription, then the realm ID will be changed for that site subscription. Otherwise, the realm ID will be changed for the farm. > If no service context is specified, the realm ID will be changed for the farm.           |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Realm** <br/> |Optional  <br/> |System.String  <br/> ||
|**ServiceContext** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------EXAMPLE-------
  
```
$c = Get-SPServiceContext -Site "http://<websiteurl>"
```

```
Set-SPAuthenticationRealm -ServiceContext $c -Realm "a686d436-9f16-42db-09b7-cb578e110ccd"
```

This example sets the authentication realm ID for the specified site subscription to the value specified by the **-Realm** parameter. 
  
> [!IMPORTANT]
> If there are no site subscriptions set up, this example will change the realm ID for the farm to the specified value. 
  
## See also

#### 

[Get-SPAuthenticationRealm](get-spauthenticationrealm.md)

