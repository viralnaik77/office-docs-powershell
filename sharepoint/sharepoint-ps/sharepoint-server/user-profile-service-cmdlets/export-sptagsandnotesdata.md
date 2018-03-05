---
title: "Export-SPTagsAndNotesData"
ms.author: kirks
author: Techwriter40
ms.date: 10/28/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e128a1ac-9159-439e-b309-89ce6f2f8e77

description: "Exports the SharePoint Newsfeed tags and notes."
---

# Export-SPTagsAndNotesData

Exports the SharePoint Newsfeed tags and notes.
  
```
Export-SPTagsAndNotesData -FilePath <String> -Site <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

----------EXAMPLE----------- 
  
```
Export-SPTagsAndNotesData -Site http://site.contoso.com -FilePath C:\TagsAndNotes.zip
```

This example creates a new .zip file called TagsAndNotes.zip, on the root of the C:\ drive, exports tags and notes from the SharePoint database for the site http://site.contoso.com, and then adds the resulting files to the TagsAndNotes.zip file .
  
## Detailed Description

Use the **Export-SPTagsAndNotesData** cmdlet to export the SharePoint Newsfeed tags and notes from the SharePoint database to a .zip file. 
  
The tags and notes are written into separate files, and then the two are compressed and added to the .zip file you specify.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _FilePath_ <br/> |Required  <br/> |System.String  <br/> |File name, including full path, that you want export the tags and notes to.  <br/> Creates a new .zip file with the name you specify. If the file already exists, the export operation will not perform and will ask you to specify a new file name.  <br/> |
| _Site_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |The URL of the root site where you want to export the tags and notes from.  <br/> You must specify a valid URL to an existing SharePoint root site. For example: http://site.contoso.com.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   

