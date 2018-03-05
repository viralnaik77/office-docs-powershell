---
title: "Update-SPHelp"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2a923949-2ef5-4f6d-a53f-d6aee8d6da65
description: "Updates the SharePoint 2016 Management Shell help files from the Microsoft Download Center, if any are available."
---

# Update-SPHelp

Updates the SharePoint 2016 Management Shell help files from the Microsoft Download Center, if any are available.
  
```
Update-SPHelp [-AssignmentCollection <SPAssignmentCollection>] [-Force <SwitchParameter>]
```

## Detailed Description

The **Update-SPHelp** cmdlet checks the Windows Download Center for updates for the SharePoint 2016 Management Shell help files against the version of the help files on the local computer. If there updates available, the cmdlet will download and install these updates. By default, the cmdlet will allow checking for updates only once every 24 hours. To override this check, use the **Force** parameter. 
  
> [!IMPORTANT]
> The computer that the cmdlet is being run on must have an internet connection. 
  
## Errors

|**Error**|**Description**|
|:-----|:-----|
|Sharepoint installation not found.  <br/> |The cmdlet was run against a computer that does not have SharePoint Server 2016 installed on it.  <br/> |
|Required registry value \<registry-path\> not found.  <br/> |The cmdlet needed to read from, or write to, a registry value and couldn't find the value.  <br/> |
|Aborting Update due to user cancellation.  <br/> |The user stopped the update process. To complete the update, try the update again using the **Force** parameter.  <br/> |
|Failed to download manifest.  <br/> |The cmdlet couldn't download the list of updates from the Microsoft Download Center server. Try the update again by using **Update-SPHelp -Force -Verbose**.  <br/> |
|Failed to download updatable help package.  <br/> |The cmdlet couldn't download the updates from the Microsoft Download Center server. Try the update again by using **Update-SPHelp -Force -Verbose**.  <br/> |
|Update cannot proceed because the manifest contains duplicate entries for version \<version\>, revision \<revision\>.  <br/> |Try the update again after 24 hours, or use the **Force** parameter.  <br/> |
   
## Example

--------------------EXAMPLE 1---------------------
  
```
Update-SPHelp
```

This example checks for updates to the help files.
  
--------------------EXAMPLE 2---------------------
  
```
Update-SPHelp -Force
```

This example over-rides the throttling logic and checks for updates to the help files even if a check was made in the last 24 hours.
  
--------------------EXAMPLE 3---------------------
  
```
Update-SPHelp -Verbose
```

This example checks for updates to the help files and provides detailed feedback for each step of the process.
  

