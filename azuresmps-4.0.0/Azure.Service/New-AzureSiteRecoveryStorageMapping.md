---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075975"
---
# New-AzureSiteRecoveryStorageMapping

## КРАТКИй обзор
Создание сопоставления между объектом хранилища Azure и объектом хранилища для восстановления.

## Максимальное

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureSiteRecoveryStorageMapping** создает сопоставление между объектом Azure Site Recovery, управляемым базой данных Azure и объектом хранилища для восстановления.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Создание сопоставления между объектом хранилища и объектом хранилища для восстановления
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

Первый командлет команды получает серверы для текущего хранилища Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryServer** .
Команда хранит серверы восстановления сайта в переменной массива $Servers.

Вторая команда получает хранилище для восстановления сайта для первого сервера в массиве $Servers и сохраняет его в $Storages.

Последняя команда создает сопоставление между основной сетью и сетью восстановления.
Команда задает Первичный объект хранилища в качестве первого элемента $Storages.
Команда задает объект хранилища для восстановления в качестве второго элемента $Storages.

## ПАРАМЕТРЫ

### -PrimaryStorage
Задает основное хранилище для сопоставления с хранилищем для восстановления.
Чтобы получить объект **ASRStorage** , используйте командлет Get-AzureSiteRecoveryStorage.

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -RecoveryStorage
Указывает объект хранилища для восстановления.
Этот командлет сопоставляет основной объект хранилища объекту хранилища, указанному в этом параметре.
Чтобы получить объект **ASRStorage** , используйте **Get-AzureSiteRecoveryStorage**.

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
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

[Get-AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)

[Get-AzureSiteRecoveryStorageMapping](./Get-AzureSiteRecoveryStorageMapping.md)

[Remove-AzureSiteRecoveryStorageMapping](./Remove-AzureSiteRecoveryStorageMapping.md)


