---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066122"
---
# Add-AzTrafficManagerEndpointConfig

## КРАТКИй обзор
Добавляет конечную точку к локальному объекту профиля диспетчера трафика.

## Максимальное

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzTrafficManagerEndpointConfig** добавляет конечную точку в локальный объект профиля диспетчера трафика Azure.
Вы можете получить профиль, используя командлеты New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.

Этот командлет работает с объектом локального профиля.
Зафиксируйте изменения в профиле диспетчера трафика с помощью командлета Set-AzTrafficManagerProfile.
Чтобы создать конечную точку и внести изменения в одну операцию, используйте командлет New-AzTrafficManagerEndpoint.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление конечной точки к профилю
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Первая команда получает профиль диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile** .
Команда хранит локальный профиль в переменной $TrafficManagerProfile.

Вторая команда добавляет конечную точку с именем Contoso в профиль, хранящийся в $TrafficManagerProfile.
Команда содержит данные конфигурации для конечной точки.
Эта команда изменяет только локальный объект.

Последняя команда обновляет профиль диспетчера трафика в Azure таким образом, чтобы он соответствовал локальному значению в $TrafficManagerProfile.

## ПАРАМЕТРЫ

### -CustomHeader
Список имен настраиваемых заголовков и пар значений для пробных запросов.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointLocation
Указывает расположение конечной точки для использования в методе маршрутизации трафика производительности.
Этот параметр применим только к конечным точкам типа ExternalEndpoints или NestedEndpoints.
Этот параметр необходимо указывать при использовании метода маршрутизации трафика производительности.

Укажите имя региона Azure.
Полный список областей Azure см. в разделе регионы Azure http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointName
Указывает имя конечной точки диспетчера трафика, которую добавляет этот командлет.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointStatus
Задает состояние конечной точки.
Допустимые значения: 

- Включаем 
- Отключает 

Если состояние включено, конечная точка проверяется на предмет работоспособности конечной точки и включена в метод маршрутизации трафика.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Геосоответствие
Список регионов, сопоставленных с этой конечной точкой, при использовании метода маршрутизации для географического трафика. [Полный список приемлемых значений](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)можно найти в документации диспетчера трафика.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinChildEndpoints
Минимальное количество конечных точек, которые должны быть доступны в дочернем профиле для того, чтобы вложенная конечная точка в родительском профиле считалась доступной.
Применимо только к конечной точке типа "NestedEndpoints".

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority (приоритет)
Задает приоритет, назначаемый диспетчером трафика конечной точке.
Этот параметр используется только в том случае, если в профиле диспетчера трафика указан метод маршрутизации трафика приоритета.
Допустимые значения — целые числа от 1 до 1000.
Более низкие значения представляют более высокий приоритет.

Если указан приоритет, необходимо задать приоритеты для всех конечных точек в профиле, но ни одна из двух конечных точек не может иметь одинаковое значение приоритета.
Если вы не укажете приоритеты, диспетчер трафика назначает конечным точкам значения приоритетов по умолчанию, начиная с единицы (1), в порядке, в котором в профиле указаны конечные точки.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetMapping
Список диапазонов адресов или подсетей, сопоставленных с этой конечной точкой при использовании метода маршрутизации трафика "подсеть".

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Target
Указывает полное DNS-имя конечной точки.
Диспетчер трафика возвращает это значение в ответах DNS, когда он направляет трафик на эту конечную точку.
Указывайте этот параметр только для типа конечной точки ExternalEndpoints.
Для других типов конечных точек укажите вместо него параметр *TargetResourceId* .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceId
Указывает идентификатор ресурса для целевого объекта.
Указывайте этот параметр только для типов конечных точек AzureEndpoints и NestedEndpoints.
Для типа конечной точки ExternalEndpoints вместо него укажите *конечный* параметр.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Указывает локальный объект **TrafficManagerProfile** .
Этот командлет изменяет этот локальный объект.
Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzTrafficManagerProfile.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Type (тип)
Указывает тип конечной точки, которую этот командлет добавляет в профиль диспетчера трафика Azure.
Допустимые значения: 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Weight
Определяет вес, который диспетчер трафика назначает конечной точке.
Допустимые значения — целые числа от 1 до 1000.
Значение по умолчанию — единица (1).
Этот параметр используется только в том случае, если профиль диспетчера трафика настроен с помощью метода маршрутизации для взвешенного трафика.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


