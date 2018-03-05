---
title: "Upgrade-SPSingleSignOnDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b7b7d9fe-548f-4059-bfe5-c771e54a697c

description: "Migrates the application definitions from Single Sign-On (SSO) database to Secure Store database as target applications."
---

# Upgrade-SPSingleSignOnDatabase

Migrates the application definitions from Single Sign-On (SSO) database to Secure Store database as target applications.
  
```
Upgrade-SPSingleSignOnDatabase -SecureStoreConnectionString <String> -SecureStorePassphrase <SecureString> -SSOConnectionString <String> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Upgrade-SPSingleSignOnDatabase** cmdlet migrates the application definitions from SSO database to Secure Store database as target applications. Use the **Upgrade-SPSingleSignOn** cmdlet to convert an SSO database to a Secure Store database. SSO is a SharePoint Server feature. SSO functionality is performed by the Secure Store Service in SharePoint Server 2016. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SecureStoreConnectionString** <br/> |Required  <br/> |System.String  <br/> |Specifies the SQL Server connection string for the Secure Store database.  <br/> |
|**SecureStorePassphrase** <br/> |Required  <br/> |System.Security.SecureString  <br/> |Specifies the passphrase used for the Secure Store database.  <br/> |
|**SSOConnectionString** <br/> |Required  <br/> |System.String  <br/> |Specifies the SQL Server connection string for the SSO database.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SecureStoreConnectionString** <br/> |Required  <br/> |System.String  <br/> ||
|**SecureStorePassphrase** <br/> |Required  <br/> |System.Security.SecureString  <br/> ||
|**SSOConnectionString** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Upgrade-SPSingleSignOnDatabase -SSOConnectionString "Data Source=oldServer;Database=SSO;Trusted_Connection=yes;" -SecureStoreConnectionString "Data Source=CONTOSO\SQLDatabase;Database=ContosoSSDatabase;Trusted_Connection=yes;" -SecureStorePassphrase "abcDEF123!@#"
```

This example migrates the SSO database at the SSO connection to a Secure Store database at the Secure Store connection.
  
## See also

#### 

[Disable-SPSingleSignOn](disable-spsinglesignon.md)

