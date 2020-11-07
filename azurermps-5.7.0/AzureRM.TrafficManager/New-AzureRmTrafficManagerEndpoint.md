---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 6117bbae035653762d99096eb8735885c0554d0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733201"
---
# New-AzureRmTrafficManagerEndpoint

## КРАТКИй обзор
Создает конечную точку в профиле диспетчера трафика.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmTrafficManagerEndpoint** создает конечную точку в профиле диспетчера трафика Azure.

Этот командлет фиксирует каждую новую конечную точку в службе диспетчера трафика.
Чтобы добавить несколько конечных точек к локальному объекту профиля диспетчера трафика и внести изменения в одну операцию, используйте командлет Add-AzureRmTrafficManagerEndpointConfig.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание внешней конечной точки для профиля
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

Эта команда создает внешнюю конечную точку с именем Contoso в профиле с именем ContosoProfile в группе ресурсов с именем ResourceGroup11.

### Пример 2: создание конечной точки Azure для профиля
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

Эта команда создает конечную точку Azure с именем Contoso в профиле с именем ContosoProfile в группе ресурсов ResouceGroup11.
Конечная точка Azure указывает на веб-приложение Azure, ИД которого Azure Resource Manager предоставляется путем URI в *TargetResourceId*.
В команде не указан параметр *EndpointLocation* , так как ресурс веб-приложения предоставляет расположение.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Полный список областей Azure см. в разделе регионы Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

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

### -EndpointStatus
Задает состояние конечной точки.
Допустимые значения: 

- Включаем 
- Отключает 

Если состояние включено, конечная точка проверяется на предмет работоспособности конечной точки и включена в метод маршрутизации трафика.

```yaml
Type: String
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
Список регионов, сопоставленных с этой конечной точкой, при использовании метода маршрутизации для географического трафика. Полный список приемлемых значений можно найти в документации диспетчера трафика.
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
Полный список областей Azure см. в разделе регионы Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя конечной точки диспетчера трафика, создаваемой этим командлетом.

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

### -Priority (приоритет)
Задает приоритет, назначаемый диспетчером трафика конечной точке.
Этот параметр используется только в том случае, если в профиле диспетчера трафика указан метод маршрутизации трафика приоритета.
Допустимые значения — целые числа от 1 до 1000.
Более низкие значения представляют более высокий приоритет.

Если указан приоритет, необходимо задать приоритеты для всех конечных точек в профиле, но ни одна из двух конечных точек не может иметь одинаковое значение приоритета.
Если вы не укажете приоритеты, диспетчер трафика назначает конечным точкам значения приоритетов по умолчанию, начиная с единицы (1), в порядке, в котором в профиле указаны конечные точки.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Имя_профиля
Указывает имя профиля диспетчера трафика, с которым этот командлет добавляет конечную точку.
Чтобы получить профиль, используйте командлеты New-AzureRmTrafficManagerProfile или Get-AzureRmTrafficManagerProfile.

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

### -ResourceGroupName
Указывает имя группы ресурсов.
Этот командлет создает конечную точку диспетчера трафика в группе, которую указывает этот параметр.

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

### -Target
Указывает полное DNS-имя конечной точки.
Диспетчер трафика возвращает это значение в ответах DNS, когда он направляет трафик на эту конечную точку.
Указывайте этот параметр только для типа конечной точки ExternalEndpoints.
Для других типов конечных точек укажите вместо него параметр *TargetResourceId* .

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

### -TargetResourceId
Указывает идентификатор ресурса для целевого объекта.
Указывайте этот параметр только для типов конечных точек AzureEndpoints и NestedEndpoints.
Для типа конечной точки ExternalEndpoints вместо него укажите *конечный* параметр.

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

### -Type (тип)
Указывает тип конечной точки, которую добавляет этот командлет к профилю диспетчера трафика.
Допустимые значения: 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: String
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
Type: UInt32
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

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Disable-AzureRmTrafficManagerEndpoint](./Disable-AzureRmTrafficManagerEndpoint.md)

[Enable-AzureRmTrafficManagerEndpoint](./Enable-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerEndpoint](./Get-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[New-AzureRmTrafficManagerProfile](./New-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpoint](./Remove-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


