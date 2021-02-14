---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241584"
---
# Add-AzTrafficManagerEndpointConfig

## SYNOPSIS
Добавляет конечную точку в локальный объект профиля Диспетчера трафика.

## СИНТАКСИС

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Cmdlet **Add-AzTrafficManagerEndpointConfig** добавляет конечную точку к локальному объекту профиля Azure Traffic Manager.
Вы можете получить профиль с помощью New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.

Этот cmdlet выполняется с объектом локального профиля.
Зафиксировать изменения в профиле диспетчера трафика с помощью Set-AzTrafficManagerProfile управления.
Чтобы создать конечную точку и зафиксировать изменение за одну операцию, используйте New-AzTrafficManagerEndpoint конечную точку.

## ПРИМЕРЫ

### Пример 1. Добавление конечной точки в профиль
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Первая команда получает профиль Диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile.**
Команда сохраняет локальный профиль в переменной $TrafficManagerProfile.

Вторая команда добавляет конечную точку contoso в профиль, $TrafficManagerProfile.
Команда содержит данные конфигурации для конечной точки.
Эта команда изменяет только локальный объект.

Конечная команда обновляет профиль Диспетчера трафика в Azure в соответствие с локальным значением в $TrafficManagerProfile.

## PARAMETERS

### -CustomHeader
Список пользовательских пар имен и значений для запросов к ветвям.

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
Определяет расположение конечной точки, используемой методом маршрутации трафика производительности.
Этот параметр применяется только к конечным точкам типа ExternalEndpoints или NestedEndpoints.
Этот параметр необходимо указать при перена указании метода маршрутизировать трафик производительности.

Укажите имя региона Azure.
Полный список регионов Azure см. в azure Regions http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (.

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
Указывает имя конечной точки Диспетчера трафика, которую добавляет этот cmdlet.

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
Определяет состояние конечной точки.
Допустимые значения: 

- Включено 
- Отключено 

Если состояние включено, конечная точка переназначна на состояние "Состояние конечной точки" и включена в способ маршрутинга трафика.

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

### -GeoMapping
Список регионов, которые были назначены этой конечной точке при использовании метода маршрутинга для географических данных. Полный список принятых значений можно получить в документации [Диспетчера трафика.](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)

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
Минимальное количество конечных точек, которые должны быть доступны в профиле ребенка, чтобы вложенная конечная точка в родительском профиле считалась доступной.
Применимо только к конечной точке типа "Вложенныеendpoints".

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

### -Priority
Определяет приоритет, который Диспетчер трафика назначает конечной точке.
Этот параметр используется только в том случае, если в профиле Диспетчера трафика настроен метод маршрутинга "Приоритетный трафик".
Допустимые значения — это значения от 1 до 1000.
Нижние значения представляют более высокий приоритет.

При указании приоритета необходимо указать приоритеты для всех конечных точек профиля, и две конечные точки не могут иметь одинаковое значение приоритета.
Если приоритеты не указаны, диспетчер трафика назначает конечным точкам значения приоритетов по умолчанию, начиная с одной (1), в том порядке, в который перечислены конечные точки профиля.

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
Список диапазонов адресов или подсетей, которые были назначены данной конечной точке при использовании метода маршрутизации трафика "Подсеть".

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
Указывает полное имя DNS конечной точки.
Диспетчер трафика возвращает это значение в ответах DNS, когда направляет трафик в эту конечную точку.
Укажите этот параметр только для типа конечной точки ExternalEndpoints.
Для других типов конечных точек укажите вместо этого параметр *TargetResourceId.*

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
Определяет ИД ресурса конечного ресурса.
Укажите этот параметр только для типов конечных точек AzureEndpoint и NestedEndpoints.
Для типа конечной точки ExternalEndpoint вместо этого укажите *целевой* параметр.

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
Определяет локальный **объект TrafficManagerProfile.**
Этот cmdlet изменяет этот локальный объект.
Чтобы получить объект **TrafficManagerProfile,** используйте Get-AzTrafficManagerProfile..

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

### -Type
Определяет тип конечной точки, которую этот cmdlet добавляет в профиль Диспетчера трафика Azure.
Допустимые значения: 

- AzureEndpoints
- Внешниеendpoints
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
Определяет вес, который Диспетчер трафика назначает конечной точке.
Допустимые значения — это значения от 1 до 1000.
Значение по умолчанию — 1(1).
Этот параметр используется только в том случае, если в профиле Диспетчера трафика настроен способ маршрутинга "Взвешемый трафик".

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## OUTPUTS

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


