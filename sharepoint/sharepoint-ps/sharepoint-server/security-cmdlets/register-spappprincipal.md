---
title: "Register-SPAppPrincipal"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/20/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f1d6b52-fd7c-46a9-b336-0d63f7851353

description: "Lets an on-premise or SharePoint Online administrator register an app principal."
---

# Register-SPAppPrincipal

Lets an on-premise or SharePoint Online administrator register an app principal.
  
```
Register-SPAppPrincipal -DisplayName <String> -NameIdentifier <String> -Site <SPWebPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Register-SPAppPrincipal** cmdlet to let an on premise farm or SharePoint Online administrator to register an app principal management service. For more information about configuring the app principle, see [Configure app authentication in SharePoint Server 2013](http://technet.microsoft.com/library/419f6a21-4968-4645-8b66-361476fd1d65.aspx).
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**DisplayName** <br/> |Required  <br/> |System.String  <br/> |Specifies the friendly name to use for the app principal that is being registered.  <br/> |
|**NameIdentifier** <br/> |Required  <br/> |System.String  <br/> |Specifies the app principal's name identifier that needs to be added to the app management service.  <br/> |
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the name of the site for the app principal object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**DisplayName** <br/> |Required  <br/> |System.String  <br/> ||
|**NameIdentifier** <br/> |Required  <br/> |System.String  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------EXAMPLE--------
  
```
$site = Get-SPSite "https://<urlofsite>"
```

```
Register-SPAppPrincipal -site $site.root -NameIdentifier "00000003-0000-0ff1-ce00-000000000000@f686d426-8d16-42db-81b7-cb578e110ccd" -DisplayName "Contoso SharePoint Online"
```

This example registers the app principal named Contoso SharePoint Online.
  
## See also

#### 

[Get-SPAppPrincipal](get-spappprincipal.md)

