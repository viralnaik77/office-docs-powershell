---
title: "Remove-SPActivityItems"
ms.author: kirks
author: Techwriter40
ms.date: 12/8/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e56753d3-e59b-4c86-86dd-e2aab52964ee

description: "Removes activity events from the published and consolidated tables."
---

# Remove-SPActivityItems

Removes activity events from the published and consolidated tables.
  
```
Remove-SPActivityItems -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind> [-AllItems <$true | $false>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-ID <Int32>] [-SearchText <String>] [-SiteSubscription <SPSiteSubscriptionPipeBind>] [-WhatIf [<SwitchParameter>]]

```

## Example

---------------EXAMPLE------------ 
  
```
$upaProxy = Get-SPServiceApplicationProxy 1232b6f7-b9ff-99ad-0cd0-fg1g67h981aq
```

```
Remove-SPActivityItems $upaProxy
```

This example removes the specific user profile service application.
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ProfileServiceApplicationProxy_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the proxy of the User Profile Service application that contains the site subscription to delete.The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a service application proxy (for example, UserProfileSvcProxy1); or an instance of a valid SPServiceApplicationProxy object.  <br/> |
| _AllItems_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether to delete events.  <br/> A value of "1" deletes all events; A value of "0", no events are deleted.  <br/> The default value is 0 (zero).  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _ID_ <br/> |Optional  <br/> |System.Int32  <br/> |Limits events deleted to those which match the specified ActivityEventID.  <br/> |
| _SearchText_ <br/> |Optional  <br/> |System.String  <br/> |Limits events deleted to those which contain SearchText in the string.  <br/> Note that the SearchText will apply to * **all** * of the XML text saved in SQL representing this activity. The text seen in a browser window may be saved in a different representation in SQL. For example, a ">" feed symbol may be represented as "&amp;gt" text in SQL, so the SearchText should reference "&amp;gt" instead of ">".  <br/> |
| _SiteSubscription_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the account under which this service should run.  <br/> This parameter is mandatory in a hosted-environment and optional in a non-hosted environment.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   

