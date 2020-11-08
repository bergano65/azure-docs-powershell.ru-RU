---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075434"
---
# Set-AzureTrafficManagerEndpoint

## КРАТКИй обзор
Обновляет свойства конечной точки в профиле диспетчера трафика.

## Максимальное

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureTrafficManagerEndpoint** обновляет свойства конечной точки в профиле диспетчера трафика Microsoft Azure.
Если конечная точка не существует в текущем профиле, этот командлет создаст его.
После того как вы добавите конечную точку, передайте результат командлету **Set-AzureTrafficManagerProfile** с помощью оператора конвейера.
Этот командлет подключается к Azure, чтобы сохранить изменения.

## ИЛЛЮСТРИРУЮТ

### Пример 1: обновление конечной точки для профиля
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

Первая команда использует командлет **Get-AzureTrafficManagerProfile** для получения профиля с именем ContosoProfile, а затем сохраняет его в переменной $TrafficManagerProfile.

Вторая команда обновляет конечную точку в профиле диспетчера трафика, который хранится в $TrafficManagerProfile.
Конечная точка имеет доменное имя ContosoApp02.cloudapp.net.
Команда также задает состояние, тип, толщину и расположение конечной точки.
Команда передает модифицированный профиль в командлет **Set-AzureTrafficManagerProfile** для подключения к Azure, чтобы сохранить изменения.

## ПАРАМЕТРЫ

### -ИмяДомена
Указывает доменное имя конечной точки, которую нужно изменить.

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

### -Location
Указывает расположение конечной точки, которую добавляет командлет.
Это должно быть расположение Azure.

Этот параметр должен содержать значения для конечных точек типа any или Type "TrafficManager" в профиле, для которого в методе балансировки нагрузки установлено значение "производительность".
Возможные значения — имена областей Azure, как указано в  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .

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

### -MinChildEndpoints
Указывает минимальное количество конечных точек, в которых должен быть подключен вложенный профиль для этой конечной точки, чтобы она считалась в сети.

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

### -Status (состояние)
Указывает состояние конечной точки наблюдения.
Допустимые значения: 

- Включаем
- Отключает

Если вы задаете значение Enabled, диспетчер трафика отслеживает конечную точку, а метод балансировки нагрузки считает это при управлении трафиком.

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

### -TrafficManagerProfile
Указывает объект профиля диспетчера трафика, для которого нужно изменить конечную точку.

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

### -Type (тип)
Указывает тип конечной точки.
Допустимые значения: 

- CloudService
- AzureWebsite
- TrafficManager

- Необходимые 

Если конечная точка AzureWebsite более одной, конечные точки должны находиться в разных центрах обработки данных.

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

### -Weight
Задает вес конечной точки, добавляемой командлетом.
Допустимый диапазон значений для этого параметра: \[ 1, 1000 \] .

Этот параметр используется только для политик балансировки нагрузки RoundRobin.

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
Этот командлет создает объект профиля диспетчера трафика, содержащий сведения об обновленном профиле.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


