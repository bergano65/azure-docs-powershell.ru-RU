---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075800"
---
# Set-AzureNetworkSecurityRule

## КРАТКИй обзор
Добавляет или изменяет правило сетевой безопасности в группе безопасности сети.

## Максимальное

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureNetworkSecurityRule** добавляет или изменяет правило сетевой безопасности Azure в сетевой группе безопасности.

## ИЛЛЮСТРИРУЮТ

## ПАРАМЕТРЫ

### -Action (действие)
Задает действие для правила сетевой безопасности.
Допустимые значения: allow и Deny.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationAddressPrefix
Указывает IP-адрес (но не классического междоменной маршрутизации (CIDR) для диапазона конечных диапазонов для правила сетевой безопасности.
Звездочка (*) задает IP-адрес.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPortRange
Указывает диапазон портов назначения для правила сетевой безопасности.
Допустимые значения состоят из целых чисел от 0 до 65535.
Вы можете задать отдельное значение или задать диапазон в формате LowerNumber-HigherNumber.
Два значения отделяются дефисом.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя для правила сетевой безопасности, которое добавляет или изменяет этот командлет.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkSecurityGroup
Указывает сетевую группу безопасности, которую изменяет этот командлет.
Чтобы получить объект **INetworkSecurityGroup** , используйте командлет Get-AzureNetworkSecurityGroup.

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Priority (приоритет)
Задает приоритет для правила сетевой безопасности.
Допустимые значения: целые числа от 100 до 4096.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет. Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

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

### -Protocol (протокол)
Задает протокол для правила сетевой безопасности.
Допустимые значения: 

- Номера 
- ТРАФИКА 
- *

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddressPrefix
Задает адрес CIDR диапазона IP-адресов источника для правила сетевой безопасности.
Звездочка (*) задает IP-адрес.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
Указывает диапазон портов источника для правила сетевой безопасности.
Допустимые значения состоят из целых чисел от 0 до 65535.
Вы можете задать отдельное значение или задать диапазон в формате LowerNumber-HigherNumber.
Два значения отделяются дефисом.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type (тип)
Указывает тип подключения для правила сетевой безопасности.
Допустимые значения: входящие и исходящие.

```yaml
Type: String
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

[Remove-AzureNetworkSecurityRule](./Remove-AzureNetworkSecurityRule.md)


