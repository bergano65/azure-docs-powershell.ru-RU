---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 8856a2f9f1a65d6d312571d75e2400a7dcf30bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566662"
---
# Set-AzureRmTrafficManagerEndpoint

## КРАТКИй обзор
Обновляет конечную точку диспетчера трафика.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmTrafficManagerEndpoint** обновляет конечную точку в диспетчере трафика Azure.
Этот командлет обновляет параметры из локального объекта конечной точки.
Вы можете указать объект конечной точки либо с помощью параметра *TrafficManagerEndpoint* , либо с помощью конвейера.

Вы можете получить локальный объект, который представляет конечную точку, используя командлет Get-AzureRmTrafficManagerEndpoint.
Измените объект на локальном компьютере, а затем используйте **Set-AzureRmTrafficManagerEndpoint** , чтобы зафиксировать изменения.

## ИЛЛЮСТРИРУЮТ

### Пример 1: обновление конечной точки
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Первая команда получает конечную точку диспетчера трафика Azure с помощью командлета **Get-AzureRmTrafficManagerEndpoint** .
Команда хранит конечную точку локально в переменной $TrafficManagerEndpoint.

Вторая команда изменяет локальную конечную точку.
Эта команда изменяет значение веса конечной точки на 20.

Третья команда обновляет конечную точку в диспетчере трафика таким образом, чтобы она соответствовала локальному значению в $TrafficManagerEndpoint.

## ПАРАМЕТРЫ

### -TrafficManagerEndpoint
Указывает локальный объект **TrafficManagerEndpoint** .
Этот командлет обновляет диспетчер трафика для соответствия этому локальному объекту.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Этот командлет принимает объект **TrafficManagerEndpoint** .

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Этот командлет возвращает объект **TrafficManagerEndpoint** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

