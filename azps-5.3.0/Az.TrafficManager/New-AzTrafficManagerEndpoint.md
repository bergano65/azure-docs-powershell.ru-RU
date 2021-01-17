---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423871"
---
# New-AzTrafficManagerEndpoint

## SYNOPSIS
Создает конечную точку в профиле Диспетчера трафика.

## СИНТАКСИС

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для **создания конечной** точки в профиле Диспетчера трафика Azure создается конечная точка.

Этот cmdlet зафиксировать каждую новую конечную точку службе Диспетчера трафика.
Чтобы добавить несколько конечных точек к локальному объекту профиля Диспетчера трафика и зафиксировать изменения за одну операцию, используйте Add-AzTrafficManagerEndpointConfig управления.

## ПРИМЕРЫ

### Пример 1. Создание внешней конечной точки для профиля
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

Эта команда создает внешнюю конечную точку с именем contoso в профиле ContosoProfile в группе ресурсов ResourceGroup11.

### Пример 2. Создание конечной точки Azure для профиля
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

Эта команда создает конечную точку Azure с именем contoso в профиле ContosoProfile в группе ресурсов ResourceGroup11.
Конечная точка Azure указывает на azure Web App, и ее ИД диспетчера ресурсов Azure задается путем URI в *TargetResourceId.*
Эта команда не указывает параметр *EndpointLocation,* так как ресурс Web App обеспечивает расположение.

## PARAMETERS

### -CustomHeader
Список пользовательских пар имен и значений для запросов к запросам на имя и значение.

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
Определяет расположение конечной точки, используемой при маршрутинге трафика с производительностью.
Этот параметр применяется только к конечным точкам типа ExternalEndpoints или NestedEndpoints.
Этот параметр необходимо указать при перена указании метода маршрутизировать трафик производительности.

Укажите имя региона Azure.
Полный список регионов Azure см. в области Azure http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (.)

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
Список регионов, которые были назначены этой конечной точке при использовании метода маршрутинга для географических данных. Полный список принятых значений можно получить в документации Диспетчера трафика.

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
Укажите имя региона Azure.
Полный список регионов Azure см. в области Azure http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (.)

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

### -Name
Указывает имя конечной точки Диспетчера трафика, которую создает этот cmdlet.

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

### -Priority
Определяет приоритет, который Диспетчер трафика назначает конечной точке.
Этот параметр используется только в том случае, если в профиле Диспетчера трафика настроен метод маршрутинга "Приоритет трафика".
Допустимые значения — это значения от 1 до 1000.
Нижние значения представляют более высокий приоритет.

При указании приоритета необходимо указать приоритеты для всех конечных точек в профиле, и две конечные точки не могут иметь одинаковое значение приоритета.
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

### -ProfileName
Имя профиля Диспетчера трафика, к которому этот cmdlet добавляет конечную точку.
Чтобы получить профиль, используйте New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.

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

### -ResourceGroupName
Указывает имя группы ресурсов.
Этот cmdlet создает конечную точку Диспетчера трафика в группе, указанной этим параметром.

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
Укажите этот параметр только для типов конечных точек AzureEndpoint и NestedEndpoint.
Для конечного типа ExternalEndpoints вместо этого укажите *целевой* параметр.

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

### -Type
Тип конечной точки, которую этот cmdlet добавляет в профиль Диспетчера трафика.
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

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


