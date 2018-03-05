---
title: "Set-SPMobileMessagingAccount"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ca94def6-f55a-4878-bb64-ee6f62373c8f

description: "Configures the specified mobile messaging account."
---

# Set-SPMobileMessagingAccount

Configures the specified mobile messaging account.
  
```
Set-SPMobileMessagingAccount [-Identity] <SPMobileMessagingAccountPipeBind> -WebApplication <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Password <String>] [-ServiceName <String>] [-ServiceUrl <String>] [-UserId <String>]
```

## Detailed Description

The **Set-SPMobileMessagingAccount** cmdlet configures the specified mobile messaging account. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPMobileMessagingAccountPipeBind  <br/> |Specifies whether to return either Short Message Service (SMS) or Multimedia Messaging Service (MMS) account information. Valid values are **SMS** and **MMS**. If you do not specify this parameter account, information is returned for both SMS and MMS.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the identity of the Web application that hosts the managed path to delete. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid Web application name (for example, WebApplication1212); or a valid name (for example, WebApp2423).  <br/> You either must specify **WebApplication** or must use the **HostHeader** switch and specify the full URL in the **Identity** parameter.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Password** <br/> |Optional  <br/> |System.String  <br/> |Specifies the password, if credentials are required for the account.  <br/> |
|**ServiceName** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the SMS service.  <br/> |
|**ServiceUrl** <br/> |Optional  <br/> |System.String  <br/> |Specifies the URL of the SMS service.  <br/> |
|**UserId** <br/> |Optional  <br/> |System.String  <br/> |Specifies the user name, if credentials are required for the account.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPMobileMessagingAccountPipeBind  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Password** <br/> |Optional  <br/> |System.String  <br/> ||
|**ServiceName** <br/> |Optional  <br/> |System.String  <br/> ||
|**ServiceUrl** <br/> |Optional  <br/> |System.String  <br/> ||
|**UserId** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
Set-SPMobileMessagingAccount -WebApplication http://sitename -Identity SMS -ServiceName SMSLink -ServiceUrl https://www.adatum.com/Service/MessagingService.asmx-UserId someone@example.com -Password password1
```

This example changes the SMS mobile account settings of the Web application,  `http://sitename`, to the following values:service name:  `SMSLink`; service URL:  `https://www.adatum.com/Service/MessagingService.asmx`; user ID:  `someone@example.com`; and password:  `password1`.
  
## See also

#### 

[Get-SPMobileMessagingAccount](get-spmobilemessagingaccount.md)

