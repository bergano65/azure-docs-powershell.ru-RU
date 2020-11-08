---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076376"
---
# Add-AzureTrafficManagerEndpoint

## КРАТКИй обзор
Добавляет конечную точку в профиль диспетчера трафика.

## Максимальное

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzureTrafficManagerEndpoint** добавляет конечную точку в профиль диспетчера трафика Microsoft Azure.
После того как вы добавите конечную точку, передайте результат командлету **Set-AzureTrafficManagerProfile** с помощью оператора конвейера.
Этот командлет подключается к Azure, чтобы сохранить изменения.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление конечной точки к профилю
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

Первая команда использует командлет **Get-AzureTrafficManagerProfile** для получения профиля с именем ContosoProfile, а затем сохраняет его в переменной $TrafficManagerProfile.

Вторая команда добавляет конечную точку в профиль диспетчера трафика, хранящийся в $TrafficManagerProfile.
Конечная точка имеет доменное имя Contoso02App.couldapp.net.
Команда также указывает, включена ли она и тип.
Команда передает объект Profile командлету **Set-AzureTrafficManagerProfile** для подключения к Azure, чтобы сохранить изменения.

### Пример 2: Добавление конечной точки с указанным расположением и весовым коэффициентом
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

Эта команда добавляет конечную точку в профиль диспетчера трафика.
Конечная точка имеет доменное имя Contoso02App.couldapp.net.
Команда также указывает, включена ли она и тип.
В команде также указывается плотность и расположение конечной точки.
Команда передает объект Profile для **настройки** подключения к Azure, чтобы сохранить изменения.

## ПАРАМЕТРЫ

### -ИмяДомена
Указывает доменное имя конечной точки, которую нужно добавить.

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
Возможные значения — имена областей Azure, как указано в https://azure.microsoft.com/regions/ .

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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Указывает объект профиля диспетчера трафика, к которому нужно добавить конечную точку.

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

Required: True
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

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Set-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


