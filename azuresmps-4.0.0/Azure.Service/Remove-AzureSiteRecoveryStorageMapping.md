---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 0A1FD05F-6573-46D8-8217-C7EA432F6742
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd8ccb634c313f487b6777a9fcb66d872b35510e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076109"
---
# Remove-AzureSiteRecoveryStorageMapping

## КРАТКИй обзор
Удаляет сопоставление объекта хранилища для хранилища сайта.

## Максимальное

```
Remove-AzureSiteRecoveryStorageMapping -StorageMapping <ASRStorageMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureSiteRecoveryStorageMapping** удаляет сопоставление объектов хранилища для текущего хранилища Azure Site Recovery.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление сопоставления между сетью и сетью восстановления
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $StorageMapping = Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PS C:\> Remove-AzureSiteRecoveryStorageMapping -StorageMapping $StorageMapping
Get-AzureSiteRecoveryServerGet-AzureSiteRecoveryStorageMappingNew-AzureSiteRecoveryStorageMapping
```

Первый командлет команды получает серверы для текущего хранилища Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryServer** .
Команда хранит серверы восстановления сайта в переменной массива $Servers.

Вторая команда получает сопоставление между двумя объектами хранилища, а затем сохраняет их в переменной $StorageMapping.
Команда задает основной сервер для сетевого сопоставления в качестве первого элемента $Servers.
Команда задает сервер для сети восстановления во втором элементе $Servers.

Последняя команда удаляет сопоставление в $StorageMapping.

## ПАРАМЕТРЫ

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

### -StorageMapping
Указывает сетевое сопоставление.
Чтобы получить **ASRStorageMapping** , используйте командлет **Get-AzureSiteRecoveryStorage** .

```yaml
Type: ASRStorageMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)


