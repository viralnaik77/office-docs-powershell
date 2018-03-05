---
title: "New-SPCentralAdministration"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/16/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b51e3b8d-b3de-4c35-bcb7-c0ade288c0e4

description: "Creates a SharePoint Central Administration web site on the local server."
---

# New-SPCentralAdministration

Creates a SharePoint Central Administration web site on the local server.
  
```
New-SPCentralAdministration [-AssignmentCollection <SPAssignmentCollection>] [-Port <Int32>] [-SecureSocketsLayer <SwitchParameter>] [-WindowsAuthProvider <String>]

```

## Example

------------------EXAMPLE 1-----------------------
  
```
New-SPCentralAdministration -Port 3000
```

This example creates the Central Administration site on HTTP Port 3000 on the local server.
  
------------------EXAMPLE 2-----------------------
  
```
New-SPCentralAdministration -Port 3000 -SecureSocketsLayer
```

This example creates the Central Administration site on the local farm to SSL Port 3000.
  
## Detailed Description

The **New-SPCentralAdministration** cmdlet creates a Central Administration web site on the local server. If you run this command on a server where there is already a Central Administration web site, this command will effectively change the port number. 
  
> [!IMPORTANT]
> If you specify a port number that has already been assigned, IIS does not start the new site until you change either the port number of the new site or the port number of the old site. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_|Optional|Microsoft.SharePoint.PowerShell.SPAssignmentCollection|Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used. > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Port_|Optional|System.Int32|Specifies the port number for Central Administration. If no port is specified, a non-conflicting port number is auto-generated.The type must be a valid port number.> [!IMPORTANT]> If you specify a port number that has already been assigned, IIS does not start the new site until you change either the port number of the new site or the port number of the old site.           |
| _SecureSocketsLayer_|Optional|System.Management.Automation.SwitchParameter|Enables Secure Socket Layer (SSL) encryption for the specified port. If you choose to use SSL, you must assign a server certificate to the Central Administration IIS web site by using the IIS administration tools. The Central Administration web application won't be accessible until you do this.The default value is **False**. > [!NOTE]> If this parameter is omitted or set to False the Central Administration site will use HTTP for the specified port.           |
| _WindowsAuthProvider_|Optional|System.String|Specifies the authorization provider for this Web application. If no authentication provider is specified, the default value **NTLM is used.**The type must be one of two values: **Kerberos**, or **NTLM**. |
   
## See also

#### 

[Set-SPCentralAdministration](set-spcentraladministration.md)
  
[Remove-SPCentralAdministration](remove-spcentraladministration.md)

