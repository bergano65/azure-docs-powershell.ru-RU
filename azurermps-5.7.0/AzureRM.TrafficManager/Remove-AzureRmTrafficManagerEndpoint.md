---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 3b3eb2fb0539be4750f4cce7dedb7cd2f26931a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563232"
---
# Remove-AzureRmTrafficManagerEndpoint

## КРАТКИй обзор
Удаляет конечную точку из диспетчера трафика.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### »
```
Remove-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DataObject
```
Remove-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmTrafficManagerEndpoint** удаляет конечную точку из диспетчера трафика Azure.

Этот командлет фиксирует каждое изменение в службе диспетчера трафика.
Для удаления нескольких конечных точек из объекта профиля диспетчера локальных данных и фиксации изменений в одной операции используйте командлет Remove-AzureRmTrafficManagerEndpointConfig.

Вы можете использовать оператор Pipeline для передачи объекта **TrafficManagerEndpoint** в этот командлет или задать объект **TrafficManagerEndpoint** с помощью параметра *TrafficManagerEndpoint* .

Кроме того, вы можете указать имя и тип конечной точки, используя параметры *Name* и *Type* вместе с параметрами *filename* и *ResourceGroupName* .

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление конечной точки из профиля
```
PS C:\>Remove-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

Эта команда удаляет конечную точку Azure с именем Contoso из профиля с именем ContosoProfile в группе ресурсов с именем ResourceGroup11.

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

### -Force
Принудительное выполнение команды без запроса подтверждения пользователя.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя конечной точки диспетчера трафика, которую удаляет этот командлет.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Имя_профиля
Указывает имя профиля диспетчера трафика, из которого этот командлет удаляет конечную точку.
Чтобы получить профиль, используйте командлет Get-AzureRmTrafficManagerProfile.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов.
Этот командлет удаляет конечную точку диспетчера трафика из профиля диспетчера трафика в группе, которую указывает этот параметр.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
Указывает конечную точку диспетчера трафика, которую удаляет этот командлет.
Чтобы получить объект **TrafficManagerEndpoint** , используйте командлет Get-AzureRmTrafficManagerEndpoint.

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Parameter Sets: Fields
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### TrafficManagerEndpoint
Параметр "TrafficManagerEndpoint" принимает значение типа "TrafficManagerEndpoint" из конвейера.

## НАПРЯЖЕНИЕ

### System. Boolean

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmTrafficManagerEndpoint](./Get-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Remove-AzureRmTrafficManagerEndpointConfig](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


