---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: 6af68da41e1d5ea212d23d0cbc2296a68a6fa7e5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065969"
---
# Update-AzDataLakeGen2Item

## КРАТКИй обзор
Обновление файлов и каталогов в свойствах, метаданных, разрешениях, списках ACL и владельцах.

## Максимальное

### ReceiveManual (по умолчанию)
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ItemPipeline
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Update-AzDataLakeGen2Item** обновляет файл или каталог в свойствах, метаданных, разрешениях, списках ACL и владельцах.
Этот командлет работает только в том случае, если для учетной записи хранения включено иерархическое пространство имен. Учетную запись такого типа можно создать с помощью командлета New-AzStorageAccount с параметром-EnableHierarchicalNamespace $true.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание объекта ACL с 3 записью ACL и рекурсивное обновление ACL для всех элементов в файловой системе
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Recurse | Update-AzDataLakeGen2Item -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser           
dir1/file1           False        1024            2020-03-23 09:29:18Z rwxrw-rw-    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxrw-rw-    $superuser           $superuser
```

Эта команда сначала создает объект ACL с 3 записью ACL (используйте параметр-InputObject для добавления записи ACL в существующий объект ACL), а затем получает все элементы в файловой системе и обновляет список ACL для элементов.

### Пример 2: обновление всех свойств файла и отображение
```
PS C:\> $file = Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" `
                 -Acl $acl `
                 -Property @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="; "ContentEncoding" = "UDF8"; "CacheControl" = "READ"; "ContentDisposition" = "True"; "ContentLanguage" = "EN-US"} `
                 -Metadata  @{"tag1" = "value1"; "tag2" = "value2" } `
                 -Permission rw-rw-rwx `
                 -Owner '$superuser' `
                 -Group '$superuser'

PS C:\> $file

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser          

PS C:\> $file.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      rw-        
False        Other                      rw-        

PS C:\> $file.Permissions

Owner        : Execute, Write, Read
Group        : Write, Read
Other        : Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\> $file.Properties.Metadata

Key  Value 
---  ----- 
tag2 value2
tag1 value1

PS C:\> $file.Properties


LastModified          : 3/23/2020 9:57:33 AM +00:00
CreatedOn             : 3/23/2020 9:29:18 AM +00:00
Metadata              : {[tag2, value2], [tag1, value1]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 1024
ContentType           : image/jpeg
ETag                  : "0x8D7CF109B9878CC"
ContentHash           : {139, 189, 187, 176...}
ContentEncoding       : UDF8
ContentDisposition    : True
ContentLanguage       : EN-US
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

Эта команда обновляет все свойства файла (ACL, разрешения, владелец, группа, метаданные, свойство может обновляться с помощью любого conbination) и отображает их в консоли PowerShell.

### Пример 3: Добавление записи ACL в каталог
```
## Get the origin ACL
PS C:\> $acl = (Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/').ACL

# Update permission of a new ACL entry (if ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry)
PS C:\> $acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rw- -InputObject $acl  

# set the new acl to the directory
PS C:\> update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/' -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

Эта команда возвращает ACL из каталога, обновляет/добавляет запись ACL и передается в каталог.
Если элемент ACL с тем же AccessControlType/EntityId/DefaultScope не существует, будет добавлена новая запись списка ACL, а в другом — разрешение на обновление существующей записи ACL.

## ПАРАМЕТРЫ

### -ACL
Устанавливает права на управление доступом POSIX для файлов и каталогов.
Создайте этот объект с помощью New-AzDataLakeGen2ItemAclObject.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Объект контекста хранилища Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileSystem
Имя файловой системы

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Группа
Задает группу владельца большого двоичного объекта.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Объект Azure Gen2 Item для обновления

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Metadata
Задает метаданные для каталога или файла.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Владелец
Задает владельца большого двоичного объекта.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Путь в указанной файловой системе, который нужно обновить.
Может быть файлом или каталогом в формате "Directory/file.txt" или "Directory1/Directory2/".
Не указывать этот параметр. Обновите корневой каталог файловой системы.

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Разрешения
Устанавливает разрешения на доступ POSIX для владельца файла, группы владельца файла и других параметров.
Каждому классу может быть предоставлено разрешение "чтение", "запись" или "выполнение".
Символические символы (rwxrw-RW-) поддерживается.
Недопустимый в сочетании с ACL.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Property
Задает свойства для каталога или файла. Поддерживаются следующие свойства файла: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.
Ниже указаны поддерживаемые свойства для каталога: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
