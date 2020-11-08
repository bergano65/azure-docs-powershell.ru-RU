---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CFAA371E-F320-4FC3-80E0-5C857E5C0998
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fbb80550acb0c743a3134a315f790bc25fb793a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076527"
---
# Get-AzureVNetSite

## КРАТКИй обзор
Получает объект списка со сведениями об виртуальных сетях Azure.

## Максимальное

```
Get-AzureVNetSite [[-VNetName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureVNetSite** получает объект списка со сведениями о виртуальных сетях Azure для текущей подписки.
Если указать имя виртуальной сети, будет возвращена только информация для этой виртуальной сети.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сведений обо всех виртуальных сетях в текущей подписке
```
PS C:\> Get-AzureVNetSite
```

Эта команда получает сведения обо всех виртуальных сетях в текущей подписке.

### Пример 2: получение сведений о конкретной виртуальной сети в текущей подписке
```
PS C:\> Get-AzureVNetSite -VNetName "MyProductionNetwork"
```

Эта команда извлекает сведения только о виртуальной сети MyProductionNetwork.

## ПАРАМЕТРЫ

### -InformationAction
Указывает, как этот командлет отвечает на информационное событие.

Для этого параметра допустимы следующие значения:

- Продолжал
- Игнорируйте
- INQUIRE
- SilentlyContinue
- Остановить
- Рвать

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Указывает переменную данных.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
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

### -VNetName
Указывает имя виртуальной сети, сведения о котором нужно вернуть.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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

[Get-AzureVNetConfig](./Get-AzureVNetConfig.md)

[Remove-AzureVNetConfig](./Remove-AzureVNetConfig.md)

[Set-AzureVNetConfig](./Set-AzureVNetConfig.md)


