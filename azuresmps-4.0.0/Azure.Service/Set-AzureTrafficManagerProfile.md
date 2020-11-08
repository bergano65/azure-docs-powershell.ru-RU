---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075794"
---
# Set-AzureTrafficManagerProfile

## КРАТКИй обзор
Обновляет свойства профиля диспетчера трафика.

## Максимальное

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureTrafficManagerProfile** обновляет свойства профиля диспетчера трафика Microsoft Azure.

Для профилей, для которых для параметра *LoadBalancingMethod* задано значение "переход на другой ресурс", вы можете определить порядок отработки отказа конечных точек, добавленных в профиль с помощью командлета Add-AzureTrafficManagerEndpoint.
Дополнительные сведения можно найти в статье пример 3.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка TTL для профиля диспетчера трафика
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

Эта команда задает срок жизни 60 секунд для объекта профиля диспетчера трафика MyTrafficManagerProfile.

### Пример 2: Настройка нескольких значений для профиля
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

Эта команда получает профиль диспетчера трафика с именем отобразите с помощью командлета **Get-AzureTrafficManagerProfile** .
В профиле используется метод балансировки нагрузки RoundRobin, срок жизни: 30 секунд, протокол монитора HTTP, порт монитора и относительный путь к профилю диспетчера трафика.

### Пример 3: упорядочение конечных точек в требуемый заказ на перемещение
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

Required: False
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

Required: False
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

Required: False
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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя профиля диспетчера трафика для обновления.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### -TrafficManagerProfile
Указывает объект профиля диспетчера трафика, который вы используете для задания профиля.

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -TTL
Указывает срок жизни (TTL) DNS, который информирует локальных имен DNS о том, сколько времени кэширование DNS-записей.
Допустимые значения — целое число от 30 до 999 999.

```yaml
Type: Int32
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

### Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition
Этот командлет создает объект профиля диспетчера трафика.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)


