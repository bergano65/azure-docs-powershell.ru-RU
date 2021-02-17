---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
ms.openlocfilehash: 209cb5ded738faabfdafc113d3d9524f7c01e927
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243176"
---
# Set-AzDataLakeGen2ItemAclObject

## SYNOPSIS
Создание и обновление объекта ACL элемента DataLake поколения 2, который можно использовать Update-AzDataLakeGen2Item этом Update-AzDataLakeGen2Item.

## СИНТАКСИС

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## ОПИСАНИЕ
С его Update-AzDataLakeGen2Item создается и обновляется объект ACL-элемента **Set-AzDataLakeGen2ItemAclObject.**
Если в входном ACL нет новой записи ACL с тем же значением AccessControlType/EntityId/DefaultScope, будет создаваться новая запись ACL, а также разрешение на обновление существующей записи ACL.

## ПРИМЕРЫ

### Пример 1. Создание объекта ACL с 3 записью ACL и обновление ACL в каталоге
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

Эта команда создает объект ACL с 3 записями ACL (с помощью параметра -InputObject для добавления записи к существующему объекту acl) и обновляет ACL в каталоге.

### Пример 2. Создание объекта ACL с 4 записями ACL и обновление разрешений для существующей записи ACL
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

Эта команда сначала создает объект ACL с 4 записями ACL, а затем снова запустите командлет с другим разрешением, но с тем же AccessControlType/EntityId/DefaultScope существующей записи ACL.
Затем разрешение на доступ к записи обновляется, но новая запись ACL не добавляется.

## PARAMETERS

### -AccessControlType
Существует четыре типа: "пользователь" предоставляет права владельцу или именоваемой пользователю, "группа" предоставляет права для владельцев или именоваемой группы, "маска" ограничивает права, предоставленные именующим пользователям и их участникам, и "другое" предоставляет права всем пользователям, не найденным ни в каких других записях.

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
Установите этот параметр, чтобы указать, что ACE принадлежит к стандарту ACL для каталога; в противном случае область неявная, а ACE принадлежит access ACL.

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
Он опущен для записей AccessControlType "mask" и "other".
Идентификатор пользователя или группы также опущен для владельца и владельца группы.

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
При входе объекта PSPathAccessControlEntry добавляет новый ACL как новый элемент входного объекта \[ \] PSPathAccessControlEntry. \[ \]

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

### -Permission
Поле разрешений — это последовательность из 3 символов, в которой первый символ — "r", чтобы предоставить доступ на чтение, второй — "w", чтобы предоставить доступ на чтение, а третий знак — "x", чтобы предоставить разрешение на выполнение.
Если доступ не предоставлен, для этого используется символ "-".

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет

## OUTPUTS

### Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
