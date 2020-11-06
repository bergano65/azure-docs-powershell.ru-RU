---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 9840476e64c78293b747f96d1a689a3ce5099bff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558991"
---
# Remove-AzureRmLoadBalancerProbeConfig

## КРАТКИй обзор
Удаляет конфигурацию зонда из подсистемы балансировки нагрузки.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Remove-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmLoadBalancerProbeConfig** удаляет конфигурацию зонда из подсистемы балансировки нагрузки.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление конфигурации зонда из подсистемы балансировки нагрузки
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $loadbalancer.

Вторая команда удаляет конфигурацию с именем MyProbe из подсистемы балансировки нагрузки в $loadbalancer.

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

### -Подсистема балансировки
Указывает подсистему балансировки нагрузки, которая содержит конфигурацию зонда, которая удаляется этим командлетом.

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя конфигурации зонда, которую удаляет этот командлет.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### PSLoadBalancer
Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSLoadBalancer

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmLoadBalancerProbeConfig](./Add-AzureRmLoadBalancerProbeConfig.md)

[Get-AzureRmLoadBalancer](./Get-AzureRmLoadBalancer.md)

[Get-AzureRmLoadBalancerProbeConfig](./Get-AzureRmLoadBalancerProbeConfig.md)

[New-AzureRmLoadBalancerProbeConfig](./New-AzureRmLoadBalancerProbeConfig.md)

[Set-AzureRmLoadBalancerProbeConfig](./Set-AzureRmLoadBalancerProbeConfig.md)


