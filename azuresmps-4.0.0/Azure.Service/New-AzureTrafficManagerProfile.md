---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076202"
---
# New-AzureTrafficManagerProfile

## КРАТКИй обзор
Создание профиля диспетчера трафика.

## Максимальное

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureTrafficManagerProfile** создает профиль диспетчера трафика Microsoft Azure.

После создания профиля, в котором вы установили для *LoadBalancingMethod* значение "переход на другой ресурс", вы можете определить порядок отработки отказа конечных точек, добавленных в профиль с помощью командлета Add-AzureTrafficManagerEndpoint.
Дополнительные сведения можно найти в статье пример 2.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Создание профиля диспетчера трафика
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

Эта команда создает профиль диспетчера трафика с именем отобразите в указанном домене диспетчера трафика с помощью метода балансировки нагрузки циклической загрузки, срок жизни 30 секунд, протокол наблюдения HTTP, мониторинг порта 80 и с указанным путем.

### Пример 2: упорядочение конечных точек в требуемый заказ на перемещение
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

В этом примере показано, как изменить порядок конечных точек, добавленных в отобразите, к нужному заказу на перемещение.

Первая команда получает объект профиля диспетчера трафика с именем отобразите и сохраняет объект в переменной $Profile.

Вторая команда повторно упорядочивает конечные точки из массива конечных точек в том порядке, в котором должна выполняться отработка отказа.

Последняя команда обновляет профиль диспетчера трафика, хранящийся в $Profile с новым порядком конечных точек.

## ПАРАМЕТРЫ

### -ИмяДомена
Задает доменное имя профиля диспетчера трафика.
Это должен быть поддомен trafficmanager.net.

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

### -LoadBalancingMethod
Указывает метод балансировки нагрузки, используемый для распространения соединения.
Допустимые значения: 

- Эффективности
- Переключения
- RoundRobin

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

### -MonitorPort
Указывает порт, используемый для отслеживания работоспособности конечной точки.
Допустимые значения: целочисленные значения больше 0 и меньше или равно 65 535.

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

### -MonitorProtocol
Указывает протокол для наблюдения за работоспособностью конечной точки.
Допустимые значения: 

- Через

- Протокол

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

### -MonitorRelativePath
Указывает путь относительно имени домена конечной точки для проверки состояния работоспособности.
Путь должен соответствовать следующим ограничениям: 

- Путь должен содержать от 1 до 1000 символов.

- Она должна начинаться с косой черты (/).

- Он не должен содержать XML-элементы \<\> .

- Оно должно содержать без двойных косых черт (//).

- Он должен содержать недопустимые escape-символы HTML.
Например,% XY.

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
Указывает имя создаваемого профиля диспетчера трафика.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -TTL
Указывает срок жизни (TTL) DNS, который информирует локальных имен DNS о том, сколько времени кэширование DNS-записей.
Допустимые значения — целые числа от 30 до 999 999.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition
Этот командлет создает объект профиля диспетчера трафика.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


