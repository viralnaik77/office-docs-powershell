---
title: "Update-SPProfilePhotoStore"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 023652c5-e25d-493e-91a3-df5a0dc1b166

description: "Updates the profile photo store to be compatible with SharePoint Server 2016."
---

# Update-SPProfilePhotoStore

 Updates the profile photo store to be compatible with SharePoint Server 2016. 
  
```
Update-SPProfilePhotoStore -MySiteHostLocation <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-CreateThumbnailsForImportedPhotos <$true | $false>] [-NewBaseUri <Uri>] [-NoDelete <$true | $false>] [-OldBaseUri <Uri>]
```

## Detailed Description

After upgrading from Office SharePoint Server 2007 to SharePoint Server 2016, run the **Update-SPProfilePhotoStore** cmdlet to ensure that the SharePoint profile photo store is compatible with SharePoint Server 2016. The **Update-SPProfilePhotoStore** cmdlet should be used only after an upgrade from Office SharePoint Server 2007 has completed. When the **Update-SPProfilePhotoStore** cmdlet is used, three thumbnail versions with predictable sizes and names are created from the original photo, the new photos are placed into the My Site Host's User Photos library, and the property value in the profile database is updated. 
  
During the operation, the original image is left as-is. If the operation fails for certain users for any reason, it continues on to the next user.
  
During the migration of profile photos from one server URL to another, one can use the **OldBaseUri** and **NewBaseUri** parameters. You just need to specify the starting portion of the URL that has changed from old to new and an attempt to rebase the profile picture URLs will occur. 
  
For example, **OldBaseUri**: http://server1/my/ProfilePhotos; **NewBaseUri**: http://server1/my/NewLocation/ProfilePhotos 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**MySiteHostLocation** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the URL for the My Site host location where the photos are to be uploaded.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CreateThumbnailsForImportedPhotos** <br/> |Optional  <br/> |System.Boolean  <br/> |Creates thumbnails for all the imported user profile pictures.  <br/> |
|**NewBaseUri** <br/> |Optional  <br/> |System.Uri  <br/> |Specifies the new URL for profile pictures. For example, http://server2/.  <br/> |
|**NoDelete** <br/> |Optional  <br/> |System.Boolean  <br/> |When the value is set to true, it specifies the deletion of imported user profile pictures after creating thumbnails for them.  <br/> |
|**OldBaseUri** <br/> |Optional  <br/> |System.Uri  <br/> |Specifies the old URL for profile pictures. For example, http://server1/.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**MySiteHostLocation** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CreateThumbnailsForImportedPhotos** <br/> |Optional  <br/> |System.Boolean  <br/> ||
|**NewBaseUri** <br/> |Optional  <br/> |System.Uri  <br/> ||
|**NoDelete** <br/> |Optional  <br/> |System.Boolean  <br/> ||
|**OldBaseUri** <br/> |Optional  <br/> |System.Uri  <br/> ||
   
## Example

------------------EXAMPLE------------------- 
  
```
Update-SPProfilePhotoStore -MySiteHostLocation http://mysites
```

This example uploads photos to a specified My Site host location.
  

