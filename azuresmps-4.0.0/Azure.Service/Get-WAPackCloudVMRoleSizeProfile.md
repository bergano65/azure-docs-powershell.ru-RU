---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076508"
---
# Get-WAPackCloudVMRoleSizeProfile

## КРАТКИй обзор
Возвращает объекты профиля размера роли облачной виртуальной машины.

## Максимальное

### Пустой (по умолчанию)
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-WAPackCloudVMRoleSizeProfile** получает объекты профиля размера роли облачной ВМ для виртуальных машин.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение профиля размера роли облачной ВМ с помощью имени
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

Эта команда получает профиль размера с именем Small.

### Пример 2: получение всех профилей размера роли виртуальной машины облака
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

Эта команда получает все профили размера.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя профиля размера роли облачной ВМ.

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет.
Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-WAPackVM](./Get-WAPackVM.md)


