---
title: "Move-SPSocialComment"
ms.author: kirks
author: Techwriter40
ms.date: 12/8/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5322b57-6c53-468e-bcff-6b03e105d814

description: "Moves social comments."
---

# Move-SPSocialComment

Moves social comments.
  
```
Move-SPSocialComment -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-NewUrl <String>] [-OldUrl <String>] [-SiteSubscription <SPSiteSubscriptionPipeBind>] [-WhatIf [<SwitchParameter>]]

```

## Example

---------------EXAMPLE------------ 
  
```
$upaProxy = Get-SPServiceApplicationProxy 1232b6f7-b9ff-99ad-0cd0-fg1g67h981aq
```

```
Move-SPSocialComments -ProfileServiceApplicationProxy $upaProxy -OldUrl "http://contoso/Pages/oldtest.aspx" -NewUrl "http://contoso/Pages/newtest.aspx"
```

This example moves social comments from oldtest.aspx to newtest.aspx.
  
## Detailed Description

This cmdlet was introduced in SharePoint Server 2010 with Service Pack 1 (SP1) and SharePoint Foundation 2010 with Service Pack 1 (SP1).
  
Use the **Move-SPSocialComment** cmdlet to move social comments from one page to another page. 
  
> [!NOTE]
> This cmdlet does not move Tags or Ratings. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ProfileServiceApplicationProxy_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the proxy of the User Profile Service application that contains the site subscription to delete.The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a service application proxy (for example, UserProfileSvcProxy1); or an instance of a valid SPServiceApplicationProxy object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _NewUrl_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the target URI to which the social notes will be moved.  <br/> |
| _OldUrl_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the source URI from which the social notes will be moved.  <br/> |
| _SiteSubscription_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the account under which this service should run.  <br/> This parameter is mandatory in a hosted-environment and optional in a non-hosted environment.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   

