---
title: "Get-SPProfileServiceApplicationSecurity"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ec9d5fad-6c67-4363-8bea-2e26901df2f5

description: "Returns permission and identity information."
---

# Get-SPProfileServiceApplicationSecurity

Returns permission and identity information.
  
```
Get-SPProfileServiceApplicationSecurity -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-SiteSubscription <SPSiteSubscriptionPipeBind>] [-Type <String>]
```

## Detailed Description

Use the **Get-SPProfileServiceApplicationSecurity** cmdlet to display permission and identity information for the following User Profile objects: 
  
- **Read individual My Sites**
  
- **Use Personal Features**
  
- **Use Social Features**
  
- **Create Personal Site**
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ProfileServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the unique identifier for the proxy.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the account under which this service should run. This parameter is mandatory in a hosted-environment and optional in a non-hosted environment.  <br/> |
|**Type** <br/> |Optional  <br/> |System.String  <br/> |Specifies the type of object to display.  <br/> The type is any one of the following values:  <br/> - **MySiteReaderACL** <br/> - **MySiteHostReaderACL** <br/> - **UserACL** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ProfileServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**Type** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

-------------------EXAMPLE--------------------
  
```
$UPAProxy = Get-SPServiceApplicationProxy -Identity "UPA proxy 1"
```

```
Get- SPProfileServiceApplicationSecurity - ProfileServiceApplicationProxy $UPAProxy -Type MySiteReaderACL
```

This example displays MySite information on  `UPA Proxy 1`.
  

