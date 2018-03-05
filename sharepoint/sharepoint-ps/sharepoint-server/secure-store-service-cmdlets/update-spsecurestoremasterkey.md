---
title: "Update-SPSecureStoreMasterKey"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 76109c55-92b5-4408-8f3f-61b616f2fd6a

description: "Changes the master key of a Secure Store Service application."
---

# Update-SPSecureStoreMasterKey

Changes the master key of a Secure Store Service application.
  
```
Update-SPSecureStoreMasterKey -Passphrase <String> -ServiceApplicationProxy <SPServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Update-SPSecureStoreApplicationServerKey** cmdlet changes the master key of a Secure Store Service application. 
  
Updating the master key is required when:
  
- A new instance of a service application is created and the database for the Secure Store service application is new or empty.
    
- The master key or passphrase has been compromised.
    
- Security guidelines require that the passphrase or key be replaced.
    
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Passphrase** <br/> |Required  <br/> |System.String  <br/> |Specifies the passphrase that is used for the Secure Store database. The passphrase that you enter is not stored. Make sure that you write down the passphrase and store it in a secure location. The passphrase will be required to add new Secure Store service servers.  <br/> |
|**ServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the proxy of the Secure Store service application that contains the master key to update.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Reencrypt** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the database for the Secure Store service application is re-encrypted. This synchronizes the master key in all servers that run an instance of the Secure Store application.  <br/> |
   
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
```

```
Update-SPSecureStoreMasterKey -ServiceApplicationProxy -Passphrase $newPassPhrase
```

This example creates a new master key for the given service application.
  
## See also

#### 

[Update-SPSecureStoreApplicationServerKey](update-spsecurestoreapplicationserverkey.md)

