---
title: "Update-SPSecureStoreApplicationServerKey"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 53234b26-d767-483a-a75f-0f2c195f8747

description: "Synchronizes the key on a Microsoft SharePoint server with the Secure Store master key."
---

# Update-SPSecureStoreApplicationServerKey

Synchronizes the key on a Microsoft SharePoint server with the Secure Store master key.
  
```
Update-SPSecureStoreApplicationServerKey -Passphrase <String> -ServiceApplicationProxy <SPServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Update-SPSecureStoreApplicationServerKey** cmdlet synchronizes the key on a SharePoint server with the master key for the Secure Store service database. 
  
Updating a server key is required when:
  
- A new SharePoint server that will run a Secure Store service instance is joined to the farm.
    
- The key stored in the server is not the key required for the current Secure Store service database (because of server or networking issues).
    
- The master key is updated but during propagation of the new key, this process fails on one or more of the servers.
    
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Passphrase** <br/> |Required  <br/> |System.String  <br/> |Specifies the passphrase that is used for the Secure Store service database.  <br/> |
|**ServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the proxy of the service application that contains the server key to synchronize.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Passphrase** <br/> |Required  <br/> |System.String  <br/> ||
|**ServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$newPassPhrase = "abcDEF123!"
Update-SPSecureStoreApplicationServerKey -ServiceApplicationProxy $contosoProxy -Passphrase $newPassPhrase
```

This example synchronizes the passphrase of the server key on a SharePoint server with the master key for the Secure Store service database.
  
## See also

#### 

[Update-SPSecureStoreMasterKey](update-spsecurestoremasterkey.md)

