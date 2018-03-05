---
title: "Restore-SPFarm"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 1/28/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8e18ea80-0830-4ffa-b6b6-ad18a5a7ab3e

description: "Restores one or more items from a backup."
---

# Restore-SPFarm

Restores one or more items from a backup.
  
```
Restore-SPFarm -Directory <String> -RestoreMethod <String> [-AssignmentCollection <SPAssignmentCollection>] [-BackupId <Guid>] [-ConfigurationOnly <SwitchParameter>] [-Confirm [<SwitchParameter>]] [-FarmCredentials <PSCredential>] [-Force <SwitchParameter>] [-Item <String>] [-NewDatabaseServer <String>] [-Percentage <Int32>] [-RestoreThreads <Int32>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Restore-SPFarm** cmdlet restores one or more items from a backup such as an individual database, Web application, or the entire farm. This cmdlet can also be used to apply a farm template to the entire farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Directory** <br/> |Optional  <br/> |System.String  <br/> |Specifies the path where SharePoint Server 2016 stored the backup package. If you have a computer on which SQL Server 2014 and an instance of SharePoint Server 2016 are installed, you can use local drive paths. This includes a basic installation. However, if SQL Server 2014 and SharePoint Server 2016 are installed on multiple computers, you must use Universal Naming Convention (UNC) share paths so that the SQL Server 2014 and SharePoint Server 2016 can read from the same location (for example, \\ _computer_name_ \volume\Backup).  <br/> The type must be either of the valid paths:  <br/> - C:\ _folder_name_ <br/> - \\ _server_name_\folder_name  <br/> > [!NOTE]> The spbr\* folders are created automatically.           |
|**RestoreMethod** <br/> |Optional  <br/> |System.String  <br/> |Specifies the method of restore to perform.  <br/> The valid values are:  <br/> - **New**; Specifies a new location to restore the content and is intended to be used when restoring to a different farm. Additional prompts will be presented to specify the new settings.  <br/> - **Overwrite**; Restores content and settings to their original locations and is intended to be used when restoring to the same farm it was backed up from. If the **Overwrite** parameter is used, a confirmation prompt is displayed. If you want the confirmation prompt suppressed, use the **Force** parameter.  <br/> |
|**ShowTree** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays which objects in the farm will be restored based on the other parameters passed to the **Restore-SPFarm** cmdlet namely the **Item** and **ConfigurationOnly** parameters. Items that will be excluded from the restore based on the other parameters passed to the **Restore-SPFarm** cmdlet will be preceded with an asterisk (*). Items that cannot be restored will be enclosed in square brackets ([ ]). A restore operation will not be performed if the **ShowTree** parameter is present.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**BackupId** <br/> |Optional  <br/> |System.Guid  <br/> |Specifies the GUID of the backup package that is to be restored. Each backup package has a unique GUID associated with it. The GUID can be seen by using the **Get-SPBackupHistory** cmdlet to view the backup history. If this parameter is not specified, the most recent backup package in the path that is specified with the **Directory** parameter is used.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890abcdef.  <br/> |
|**ConfigurationOnly** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies settings only (no data) will be restored from the backup package and applied to objects on the destination farm.  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**FarmCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the credentials that will be used for all components being restored. For example, the application pool credentials for Web applications being restored. If an application pool being restored already exists in the farm, the credentials specified by the **FarmCredentials** parameter is ignored when restoring that application pool.  <br/> |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Suppresses the prompt warning that you will overwrite components when you perform an overwrite restore operation.  <br/> |
|**Item** <br/> |Optional  <br/> |System.String  <br/> |Indicates the part of the backup package to be restored. You can use the full farm path notation as displayed by the **ShowTree** parameter or the name of the target component in the path if it has a unique name. If multiple items match the name, the full path must be provided. Surround the item or path in double quotation marks if it contains a space. If this parameter is absent, the entire backup package is restored.  <br/> The type must be a valid item, such as:  <br/> Farm\Microsoft SharePoint Foundation Web Application\SharePoint - 80  <br/> |
|**NewDatabaseServer** <br/> |Optional  <br/> |System.String  <br/> |Specifies a valid SQL Database Server name. If specified, will be used as a default Database Server name for all databases within the restore operation.  <br/> This parameter is only valid when restoring as new. It is not valid for overwrite restores.  <br/> |
|**Percentage** <br/> |Optional  <br/> |System.Int32  <br/> |Requests that progress updates about the restore operation be displayed in increments of that percentage. For example, a value of **5** displays restore progress updates at every 5 percent completed, and a value of **10** displays restore progress updates at every 10 percent completed.  <br/> Note: Progress will only be displayed in the output if the - **Verbose** parameter is specified. Otherwise, you may see the progress in the restore log file.  <br/> This percentage is not precise and the actual progress updates might be lower or higher than requested.  <br/> For a very large database, **1** is the recommended value.  <br/> The type must be an integer value between **1** and **100**.  <br/> The default value is **5**.  <br/> |
|**RestoreThreads** <br/> |Optional  <br/> |System.Int32  <br/> |The number of threads that should be used during the restore.  <br/> The fewer the restore threads, the easier it is to understand the restore log. However, the more restore threads, the more components can be restored in parallel, potentially resulting in a faster restore.  <br/> The valid range is between 1 and 10. The default value is 3.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

-------------------EXAMPLE 1----------------------- 
  
```
Restore-SPFarm -Directory \\file_server\share\Backup -BackupId 12345678-90ab-cdef-1234-567890abcdef -RestoreMethod new -ConfigurationOnly
```

This example restores the configuration settings from the backup package in the \\file_server\share\Backup directory to the farm.
  
-------------------EXAMPLE 2----------------------- 
  
```
Restore-SPFarm -ShowTree -Directory \\file_server\share\Backup -BackupId 12345678-90ab-cdef-1234-567890abcdef -Item "Microsoft SharePoint Foundation Web Application" -Verbose
```

This example show which components of the farm would be restored under the  `Microsoft SharePoint Foundation Web Application` node, but does not actually restore them. 
  
-------------------EXAMPLE 3----------------------- 
  
```
Restore-SPFarm -Directory C:\Backup -BackupId 12345678-90ab-cdef-1234-567890abcdef  -RestoreMethod overwrite -RestoreThreads 10 -Force
```

This example restores a farm by using  `10` threads and suppresses the  `overwrite` warning. 
  
## See also

#### 

[Backup-SPFarm](backup-spfarm.md)
  
[Backup-SPConfigurationDatabase](backup-spconfigurationdatabase.md)
  
[Get-SPBackupHistory](get-spbackuphistory.md)

