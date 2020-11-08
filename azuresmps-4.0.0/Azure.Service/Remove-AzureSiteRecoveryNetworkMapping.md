---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076110"
---
# Remove-AzureSiteRecoveryNetworkMapping

## КРАТКИй обзор
Удаляет Сетевое сопоставление из хранилища сайта.

## Максимальное

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureSiteRecoveryNetworkMapping** удаляет Сетевое сопоставление из текущего хранилища Azure Site Recovery.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление сопоставления между сетью и сетью восстановления
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

Первый командлет команды получает серверы для текущего хранилища Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryServer** .
Команда хранит серверы восстановления сайта в переменной массива $Servers.

Вторая команда получает сопоставление между основной сетью и сетью восстановления, а затем сохраняет его в переменной $NetworkMapping.
Команда задает основной сервер для сетевого сопоставления в качестве первого элемента $Servers.
Команда задает сервер для сети восстановления во втором элементе $Servers.

Последняя команда удаляет Сетевое сопоставление в $NetworkMapping.

### Пример 2: Удаление сопоставления сети и сети виртуальной машины Azure
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

Первый командлет команды получает серверы для текущего хранилища для восстановления сайта.
Команда хранит серверы восстановления сайта в переменной массива $Servers.

Вторая команда получает сопоставление между основной сетью и сетью виртуальной машины Azure, а затем сохраняет его в переменной $NetworkMapping.
Команда задает основной сервер для сети в качестве первого элемента $Servers.
Команда задает параметр *Azure* .
Таким образом, команда получает сопоставление с сетью виртуальной машины Azure.

Последняя команда удаляет Сетевое сопоставление в $NetworkMapping.

## ПАРАМЕТРЫ

### -NetworkMapping
Указывает сетевое сопоставление для удаления.

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

[Get-AzureSiteRecoveryNetworkMapping](./Get-AzureSiteRecoveryNetworkMapping.md)

[New-AzureSiteRecoveryNetworkMapping](./New-AzureSiteRecoveryNetworkMapping.md)

[Get-AzureSiteRecoveryServer](./Get-AzureSiteRecoveryServer.md)


