---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065697"
---
# Set-AzDataLakeGen2ItemAclObject

## КРАТКИй обзор
Создает или обновляет объект ACL элемента Gen2, который можно использовать в командлете Update-AzDataLakeGen2Item.

## Максимальное

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzDataLakeGen2ItemAclObject** создает и ОБНОВЛЯЕТ объект ACL элемента Gen2, который можно использовать в командлете Update-AzDataLakeGen2Item.
Если новая запись ACL с тем же AccessControlType/EntityId/DefaultScope не существует в входных данных ACL, будет создана новая запись списка ACL, а в другом — разрешение на обновление существующей записи ACL.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание объекта ACL с 3 записью ACL и обновление списка ACL в каталоге
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

Эта команда создает объект ACL с 3 записями ACL (используйте параметр-InputObject для добавления записи ACL в существующий объект ACL) и обновляет список ACL в каталоге.

### Пример 2: создание объекта ACL с четырьмя записями ACL и обновление разрешений существующей записи ACL
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

Эта команда сначала создает объект ACL с четырьмя записями ACL, а затем повторно запускает командлет с различными разрешениями, но же AccessControlType/EntityId/DefaultScope существующей записи ACL.
После этого разрешение записи ACL будет Обновлено, но новая запись ACL не будет добавлена.

## ПАРАМЕТРЫ

### -AccessControlType
Существует четыре типа: "пользователь" предоставляет права владельцам или именованным пользователям, "Группа" предоставляет права для группы владельца или именованной группы, "маска" ограничивает права, предоставленные именованным пользователям и членам групп, а "другой" предоставляет права всем пользователям, не найденным в других записях.

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultScope
Установите этот параметр, чтобы указать, что ACE входит в ACL по умолчанию для каталога; в противном случае область является неявной и ACE принадлежит к ACL Access.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EntityId
Идентификатор пользователя или группы.
Оно опущено для записей AccessControlType "маска" и "другое".
Идентификатор пользователя или группы также не указывается для владельца и группы-владельца.

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
При вводе объекта PSPathAccessControlEntry добавит \[ \] новый список ACL в качестве нового элемента входного \[ \] объекта PSPathAccessControlEntry.

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

### -Разрешения
Поле разрешения является 3-символьной последовательностью, где первый символ "r" для предоставления доступа на чтение, второй символ — "w" для предоставления доступа на запись, а третий — "x" для предоставления разрешения на выполнение.
Если доступ не предоставлен, знак "-" используется для того, чтобы отметить, что разрешение запрещено.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSPathAccessControlEntry

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
