---
title: "New-SPODataConnectionSetting"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6447c39c-6de4-4df7-9065-4ce7d26540e7

description: "Creates a new Business Data Connectivity service connection."
---

# New-SPODataConnectionSetting

Creates a new Business Data Connectivity service connection.
  
```
New-SPODataConnectionSetting -AuthenticationMode <PassThrough | RevertToSelf | Credentials | WindowsCredentials | DigestCredentials | ClientCertificate | Anonymous> -Name <String> -ServiceAddressURL <Uri> -ServiceContext <SPServiceContextPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-ExtensionProvider <String>] [-SecureStoreTargetApplicationId <String>]
```

## Detailed Description

Use the **New-SPODataConnectionSetting** cmdlet to create a new Business Data Connectivity service connection and its associated metadata properties in the farm. To see the metadata settings, use the [Get-SPODataConnectionSettingMetaData](get-spodataconnectionsettingmetadata.md) cmdlet. 
  
> [!NOTE]
> This cmdlet applies to an on-premises environment only. You cannot use this command in the SharePoint Online Management Shell. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AuthenticationMode** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.SystemSpecific.OData.ODataAuthenticationMode  <br/> |Specifies the type of authentication mode required for the Business Connectivity Services connection.  <br/> The value for the authentication mode is any one of the following options: ****|||
|:-----|:-----|
|--PassThrough  <br/> ||
|--RevertToSelf  <br/> ||
|--Credentials  <br/> ||
|--WindowsCredentials  <br/> ||
|--DigestCredentials  <br/> ||
|--ClientCertificate  <br/> ||
|--Anonymous  <br/> ||
   
|
|**ServiceAddressURL** <br/> |Required  <br/> |System.Uri  <br/> |Specifies the URL for the OData service. The URL does not have be Internet facing. This is the final destination from which data is retrieved.  <br/> |
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context which is in the form of an instance of an **SPServiceContext** object, an **SPSiteAdministration** object identifier, or a **SPSite** object. An example of a service context value is an identifier from the ID field, a string identifier, a URI, or a string representation of a GUID.  <br/> |
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the Business Connectivity Services connection object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**ExtensionProvider** <br/> |Optional  <br/> |System.String  <br/> |Extends the functionality provided by the OData connector in Business Connectivity Service as well as provides the fully qualified assembly name of an OData extension provider. Fully qualified assembly name should contain following parameters in this order:  <br/> Namespace.Class, Assembly Name, Version, Culture and Public Key. E.g. "Contoso.ExtensionProvider.Server, Contoso.ExtensionPRovider, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31ba4812ca364d35". To clear the value of ExtensionProvider, provide an empty string, for example, "".  <br/> |
|**SecureStoreTargetApplicationId** <br/> |Optional  <br/> |System.String  <br/> |Specifies the Secure Store Target Application ID. Works in conjunction with the **AuthenticationMode** parameter.  <br/> The value for the **SecureStoreTargetApplicationId** parameter is any one of the following options:  <br/> --Credentials  <br/> --WindowsCredentials  <br/> --DigestCredentials  <br/> --ClientCertificate  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AuthenticationMode** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.SystemSpecific.OData.ODataAuthenticationMode  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**ServiceAddressURL** <br/> |Required  <br/> |System.Uri  <br/> ||
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**ExtensionProvider** <br/> |Optional  <br/> |System.String  <br/> ||
|**SecureStoreTargetApplicationId** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

--------------EXAMPLE-------------- 
  
```
New-SPODataConnectionSetting -Name "ContosoServiceApp" -ServiceContext "http://contoso" -ServiceAddressURL "https://expensereporting.cloudapp.net/expensereporting.svc" -AuthenticationMode "Credentials" -SecureStoreTargetApplicationId "DallasUserName" -ExtensionProvider "Contoso.ExtensionProvider.Server, Contoso.ExtensionPRovider, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31ba4812ca364d35"

```

This example creates a new Business Data Connectivity service connection named ContosoServiceApp.
  
In this process, a Microsoft Business Connectivity Services connection metadata object is created.
  
## See also

#### 

[Get-SPODataConnectionSetting](get-spodataconnectionsetting.md)
  
[Remove-SPODataConnectionSetting](remove-spodataconnectionsetting.md)
  
[Set-SPODataConnectionSetting](set-spodataconnectionsetting.md)

