---
title: "New-SPSecureStoreTargetApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0b520f39-d2a4-4729-b6c1-8ffc17967b9d

description: "Creates a new Secure Store target application."
---

# New-SPSecureStoreTargetApplication

Creates a new Secure Store target application.
  
```
New-SPSecureStoreTargetApplication -ApplicationType <Individual | Group | IndividualWithTicketing | GroupWithTicketing | RestrictedIndividual | RestrictedGroup> -FriendlyName <String> -Name <String> [-AssignmentCollection <SPAssignmentCollection>] [-ContactEmail <String>] [-SetCredentialsUri <Uri>] [-TimeoutInMinutes <Int32>]
```

## Detailed Description

The **New-SPSecureStoreTargetApplication** cmdlet creates a new Secure Store Target application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationType** <br/> |Required  <br/> |Microsoft.BusinessData.Infrastructure.SecureStore.TargetApplicationType  <br/> |Specifies the type of target application.  <br/> The type must be one of the following: **Individual**, **Group**, **IndividualWithTicketing**, **GroupWithTicketing**, **RestrictedIndividual**, or **RestrictedGroup**.  <br/> |
|**FriendlyName** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the new target application.  <br/> |
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the display name of the new target application.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**ContactEmail** <br/> |Optional  <br/> |System.String  <br/> |Specifies the contact information for the target application.  <br/> |
|**SetCredentialsUri** <br/> |Optional  <br/> |System.Uri  <br/> |Specifies the URI for setting the user application credentials.  <br/> The type must be a valid URI, in the form file:\\server_name\sitedocs.  <br/> |
|**TimeoutInMinutes** <br/> |Optional  <br/> |System.Int32  <br/> |The time, in minutes, a ticket is valid if it is not redeemed by the target application. Make sure that the ticket time-out value is long enough to last between the time when the ticket is issued to the time that it is redeemed The default value is **2**.  <br/> The type must be a valid integer.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationType** <br/> |Required  <br/> |Microsoft.BusinessData.Infrastructure.SecureStore.TargetApplicationType  <br/> ||
|**FriendlyName** <br/> |Required  <br/> |System.String  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**ContactEmail** <br/> |Optional  <br/> |System.String  <br/> ||
|**SetCredentialsUri** <br/> |Optional  <br/> |System.Uri  <br/> ||
|**TimeoutInMinutes** <br/> |Optional  <br/> |System.Int32  <br/> ||
   
## Example

------------------EXAMPLE 1------------------
  
```
New-SPSecureStoreTargetApplication -Name "ContosoTargetApplication" -FriendlyName "Contoso Target Application" -ApplicationType Group
```

This example creates a new group type target application with the given name and friendly display name.
  
## See also

#### 

[New-SPSecureStoreApplicationField](new-spsecurestoreapplicationfield.md)

